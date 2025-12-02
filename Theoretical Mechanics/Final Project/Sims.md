![[Pasted image 20251121230154.png]]
![[Pasted image 20251121230210.png]]

``` Python
%% Planer 3 body problem

% Aly Rajan and Sorin Jayaweera

% 11/21/2025

% things to figure out:

% dsolve, matlabFunction, odeFunction, ode45

clear

close all

clc

%% Variable setup

syms x(t) y(t)

syms m_s m_e m_a G Omega

syms f a

%% Lagrangian

xdot = diff(x(t), t);

ydot = diff(y(t), t);

r_sun = sqrt((x + f*a)^2 + y^2);

r_earth = sqrt((x - (1-f)*a)^2 + y^2);

L = 1/2*m_a*(xdot^2 + ydot^2) + 1/2 * m_a * Omega^2 * (x^2 + y^2)...

+ m_a*Omega*(x*ydot - y*xdot) + G*m_s*m_a/r_sun + G*m_e*m_a/r_earth;

%% Diff Eqs

dL_dx = diff(L, x);

dL_dy = diff(L, y);

dL_dxdot = diff(L, xdot);

dL_dydot = diff(L, ydot);

d_dtxdot = diff(dL_dxdot, t);

d_dtydot = diff(dL_dydot, t);

%%

% Now we have the lagrangian for the motion of the asteroid in the frame

% with the sun and earth are stationary, which we can solve for

xdiffeq = d_dtxdot == dL_dx;

ydiffeq = d_dtydot == dL_dy;

[V, S] = odeToVectorField([xdiffeq, ydiffeq]);

M = matlabFunction(V, 'vars', {'t', 'Y', 'Omega', 'G', 'm_a', 'm_e', 'm_s', 'a', 'f'});

%% Parameters

Omega = 1; % [s^-1]

G = 6.67e-11; % [m^3 kg^-1 s^-2]

m_a = 1e-5; % [kg]

m_e = 1; % [kg]

m_s = 100; % [kg]

a = 1; % [km]

f = m_e/(m_s+m_e); % dimensionless

odefun = @(t,Y) M(t, Y, Omega, G, m_a, m_e, m_s, a, f);

%% Initial Conditions

x0 = 1;

y0 = 10;

xdot0 = 0;

ydot0 = 0;

initconds = [y0,ydot0,x0,xdot0];

%% Evaluating

t0 = 0;

tf = 1000000;

[t_soln, z_sol] = ode45(odefun, [t0,tf], initconds);

y_soln = z_sol(:,1);

ydot_soln = z_sol(:,2);

x_soln = z_sol(:,3);

xdot_soln = z_sol(:,4);

%% To the inertial frame (not the rotating one)

x_inertial = x_soln.*cos(Omega.*t_soln) - y_soln .* sin(Omega.*t_soln);

xdot_inertial = xdot_soln * cos(Omega.*t) - ydot_soln * sin(Omega.*t) - x_soln * Omega * sin(Omega.*t) - y_soln .* Omega .* cos(Omega .* t);

y_inertial = x_soln .* sin(Omega .*t_soln) + y_soln .* cos(Omega.*t_soln);

ydot_inertial = xdot_soln .* sin(Omega.*t_soln) + ydot_soln .* cos(Omega .* t_soln) + x_soln .* Omega .* cos(Omega*t_soln) - y_soln .* Omega.*sin(Omega.*t_soln);

%%

figure;

plot(x_soln,y_soln);

hold on;

scatter(x_soln(1),y_soln(1), 'filled');

xlabel('X Pos [km]');

ylabel('Y pos [km]');

title('Asteroid Motion in the Planar 3-Body Problem');

grid on;

axis equal;

%%

figure;

plot(x_inertial,y_inertial);

hold on;

% scatter(x_soln(1),y_soln(1), 'filled');

xlabel('X Pos [km]');

ylabel('Y pos [km]');

title('Asteroid in Inertial Frame');

grid on;

axis equal;

%%

figure

subplot(2,2,1)

plot(t_soln, z_sol(:,1))

title('Y vs time')

subplot(2,2,2)

plot(t_soln, z_sol(:,2))

title('Ydot vs time')

subplot(2,2,3)

plot(t_soln, z_sol(:,3))

title('X vs time')

subplot(2,2,4)

plot(t_soln, z_sol(:,4))

title('X dot vs time')
```