% ****** Modification of "apssamp.tex" ******
%   That file:  Copyright (c) 2009, 2010 The American Physical Society.
\documentclass[twocolumn,10pt,amsmath,amssymb,aps,pre]{revtex4-1}
\usepackage{graphicx}% Include figure files - can be .pdf, .png, etc.
\usepackage{dcolumn}% Align table columns on decimal point
\usepackage{bm}% bold math
\usepackage{siunitx}% SI units package
\usepackage{subcaption}
\usepackage{todonotes}
%\usepackage{fancyhdr}

\newcommand{\comment}[1]{\textcolor{red}{#1}}

\begin{document}

\title{A characterization of the Sodium Doublet and Pressure Broadened Mercury} 
\author{Sorin Jayaweera}
\affiliation{Harvey Mudd College}

\collaboration{Lab partner: Annika Larson}

\date{8 April 2026}

\begin{abstract}
Fourier transform spectroscopy was used to find the difference in sodium emission spectra due to spin orbit coupling, and therefore the energy associated with the interaction. The sodiumm doublet splitting was measured to have a wavelength difference of $\Delta \lambda=0.58 \pm 0.0064$. The same technique was used to characterize the effects of pressure broadening on the spectral emission of a mercury light source. The interaction time was found from the trend in visibility at distances near equal path length, yielding pressure broadening of $6 \pm 1.4 \times 10^{11}$ Hz.

\end{abstract}

\maketitle

% \thispagestyle{fancy}



\section{\label{s:intro}Introduction}

Fourier transform spectroscopy is a technique that can be used to resolve the dominant frequencies within a light source. In this paper, Fourier spectroscopy is first demonstrated on the well characterized sodium doublet emission due to spin-orbit coupling. We then characterize the pressure broadening of a mercury light source by using the interference fringes.

\section{\label{s:fts} Fourier Transform Spectroscopy}
The spatial Fourier transform of the intensity of light out of a Michaelson interferometer gives the spectrum of that light source, following the relationship
\[
P(\omega) = \frac{2}{\pi} \int_{0}^{\infty} \left[ \frac{I(\tau)}{\left< I \right> }-1\right] \cos \omega \tau d\tau
\]
where  $\tau= \frac{2d}{c}$ is the phase difference between the two arms of the Michaelson interferometer, and $d$ is the difference in path length. 

\section{\label{Experimental Setup} Experimental setup}
The light source for each respective experiment - a Sodium or Mercury lamp - was placed in a dark room shrouded in a dark box with a small slit to direct light from the lamp to the interferometer. The optical paths consisted of an optical filter, followed by a  half wave beam-splitter. The beam-splitter leads to two paths - one towards a compensation plate and a fixed mirror on an adjustable rail (variable with a micrometer), and one path with only an fixed but rotatable mirror to align the mirrors and account for angle differences. Each path of light reflects off of their respective mirrors, and recombine at the beamsplitter, where light may be sent towards a photo-diode,  as shown in Fig\ref{fig:interferometerdiagram}. The 

When there is interference between the two paths, there are multiple fringes which appear in the image after combination, due to the difference in path length on the order of wavelengths of light due to the tilting of the mirrors. When the path length is exactly equal across and up-down along the mirrors, circular fringes appear. These fringes are due to the difference in angles that the light could arrive at the interferometer from - slightly angled light will have a slightly longer path. The variation in path length due to these angles causes circular fringes. \footnote{I think this is true, I realized that I don't actually understand why we get more than a single variation between dark and light if we don't have this reason.} 


\begin{figure}
    \centering
    \includegraphics[width=0.5\linewidth]{interferometer.png}
    \caption{Caption}
    \label{fig:interferometerdiagram}
\end{figure}



\section{Sodium Doublet}

\subsection{Background}
The intensity of light at after the interferometer for two frequencies interfering is given by

\[
I \propto 2\left[ 1+\cos(\omega \tau)\cos\left(  \frac{\Delta \omega}{2}\tau \right) \right]
\]
where $\omega$ is the average frequency of the sodium doublet, and $\Delta \omega$ is the difference in frequency. This is a slow varying envelope cosine, with a high frequency cosine tracing out the envelope, as shown in Fig. \ref{fig:sodium_drawing}. Visibility is a time average of intensity, over which the rapidly varying cosine for minute changes in path length is not visible. The maximum visibility points are peaks of the slowly varying cosine. 



 The slow cos has a frequency $\frac{\Delta \omega}{2}$, and the peaks are spaced apart by $d$, which corresponds to a time difference $\Delta \tau = 2 \frac{\Delta d}{c}$ because the light has to travel the difference in distance between the arms twice. For $\cos \frac{\Delta \omega}{2}$ to go from zero crossing to zero crossing, 

\begin{align}
\frac{\Delta \omega}{2} \Delta \tau  & = \pi \\
\text{ so, }\Delta \omega & = \frac{\pi c}{ \Delta d }
\end{align}


\begin{figure}
    \centering
    \includegraphics[width=0.5\linewidth]{sodium_demograph.png}
    \caption{A graphical depiction of the product between a high frequency and low frequency cosine, the predicted intensity as a function of tau}
    \label{fig:sodium_drawing}
\end{figure}
The distance between maximum visibility to the minimum visibility must traverse a phase of $\frac{\pi}{2}$ along the slow varying cosine.

\begin{align}
     2\pi \left( \frac{1}{\lambda_{1}}+ \frac{1}{\lambda_{2}} \right)d = \frac{\pi}{2} \\ d = \frac{1}{\frac{4}{\lambda_{1}}+ \frac{4}{\lambda_{2}}}
\end{align}

 
For previously found wavelengths of the sodium doublet, $\lambda_{1}= 589.0$ nm and $\lambda_{2}=589.6$ nm, we would expect $\Delta d $, the spacing between successive maximum visibilities, to be $0.3$ mm. This experiment is a test of previous literature in characterizing this $0.3$ mm spacing.



\subsection{Procedure}

The sodium lamp was turned on. An observer viewed the combined light output from the interferometer as the adjustable arm was translated. Once interference fringes were observed, the adjustable mirror was used to ensure circular fringes across the field of view. With the mirrors in position, the translating arm was slowly translated, and the path length positions at which fringes fully disappeared were recorded. The stage was translated across through the positions of 10 interference minima 5 times, and the observed positions of minimal interference between the two frequencies of light.  The greatest visibility locations with no interference visible occur at the same frequency as the maximum interference, but were easier to visually distinguish. 



\subsection{Results}


\begin{figure}
\begin{subfigure}[h]{0.4\linewidth}
\includegraphics[width=\linewidth]{sodium_fit.png} 
\caption{The average time delay of successive interference}
\end{subfigure}
\hfill
\begin{subfigure}[h]{0.4\linewidth}
\includegraphics[width=\linewidth]{sodium_fit_distance.png}
\caption{The average positions of interference minimas}
\end{subfigure}%
\caption{Linear fits for minimum spacing in the Sodium lamp interferometer}
\label{fig:sodiumfit}
\end{figure}


A linear fit of $\Delta \tau$ versus minimum number shows a near constant spacing of 1.94 $\pm0.0024 \,ps$ was observed between the locations of minimal interference / maximum visibility locations, corresponding to path spacing of $0.291 \pm \, 0.00032$ mm. This equates to a difference in frequency betewen the sodium doublet $\Delta \lambda=0.58 \pm 0.0064$ nm. This is close to the previously determined literature path spacing $0.3$ mm with $\Delta \lambda_{\text{literature}}$ of $0.6$ nm. with variation accountable due to mechanical drift in our micrometer. The uncertainties are likely under-reported\footnote{We didn't measure the actual uncertainty from drift to add in quadrature - if I really didn't want to do that, how would I say that I know my uncertainties are too small?}.



\section{ Mercury Pressure broadening}
\subsection{Background}

When atoms collide with each other or are within a close neighborhood, they change the potential and broaden atomic transitions. At each collision of particles, a random phase shift is added to the emission. Due to this, the coherence time of pressure broadened light sources is far smaller. The broadening corresponds to a larger half width at half maximum $\frac{1}{\tau_{p}}$, where $\tau_{p} $ is the average time in seconds between collisions of mercury atoms . The wavelength of mercury emission is known to be $\lambda = 546 $nm. 

Due to broadening, the power as a function of $\omega$ is predicted to be 

\[
P(\omega) = \frac{1}{\pi} \frac{\frac{1}{\tau_{p} }}{(\omega-\omega_{0})^{2}+ \left( \frac{1}{\tau_{p} } \right)^{2}}
\]

This would give the intensity as a function of the path length phase as
\[
I(\tau) = \left< I \right> \left[1+e^{\left(-\frac{\tau}{\tau_{p} }\right)}\cos(\omega_{0}\tau)\right]
\]

We can see, then, that the visibility V - the time average of intensity - depends on $\tau_{p}$ as 

\[
V  \propto e^{\frac{-\tau}{\tau_{p }} }
\]
Therefore, the slope of  $\ln(V)$ as a function of $\tau$ is theorized to be $-\frac{1}{\tau_{p}}$. 

\subsection{Procedure}
\subsubsection{Finding equal path length}
Due to the small coherence time, we use visible sodium fringes and the naked eye to find equal path length between the arms of the interferometer. Each path of light is really a spherically expanding wavefront. The longer the distance that the wavefront travels, the more it will flatten out. Interference fringes appear at locations where both the paths of light intersect and the phase of waves cancel. At equal path length, the two paths of light have wavefronts which have expanded in the same way. Any fringes would be due to tiny differences in path length due to angled mirrors. Moving the translating arm of the interferometer closer to equal path length will make fringes appear to fall towards the center. At equal path length, the fringes will have the biggest width due to the largest amount of overlap between the two paths of light. Beyond this, the fringes will appear to fall out from the center, as the translating arm will now have a more expanded wavefront compared to the stationary arm. 

Equal path length can be located between the sodium doublet interference minimums where fringes transition between moving towards the center with increasing path length to moving away from the center, \ref{fig:fringewaves}. The wavefronts have total destructive interference at intersection points, and interfere partially in the neighborhood around those points. The more similar the curvature, the larger the area where the wavefronts have similar phase and interfere. 

\begin{figure}
    \centering
    \includegraphics[width=0.5\linewidth]{fringewaves.png}
    \caption{A depiction of two wave fronts of the same phase which have traveled different lengths. The longer the wave travels, the wider the wavefront. As the waves get closer to equal path length, the fringe intersection points move radially. }
    \label{fig:fringewaves}
\end{figure}
The equal path length was identified to be between 7.24 and 7.42  mm, although is suspected to have become a lower mm reading due to drift on the micrometer. 

\subsubsection{Measuring Mercury Visibility}
A photodiode was placed downstream of the optic path to measure the intensity of light. The adjustable arm path length was translated from below to above equal path length in $50$ nm increments. At each position,  the table and interferometer were lightly pressed with a finger to minor adjust the path length. Due to the short coherence time, the interference fringes are only. Close to equal path length, small variations in the path  cause fringes to cross the aperture of the photo-diode, causing dramatic variation in the intensity of light for small disturbances.  The variation in the intensity of light was recorded as the total voltage range swept from perturbations due to this light taping. The interferometer arm distance was reset after each round of tapping for 5 rounds, after which the micrometer was advanced to the next position 50 nm away.  


\subsection{Results}
\begin{figure}
\begin{subfigure}[h]{0.4\linewidth}
\includegraphics[width=\linewidth]{fit_left.png} 
\caption{Fit of $\ln(\text{Intensity})$ when the translatable arm was less than equal path length}
\end{subfigure}
\hfill
\begin{subfigure}[h]{0.4\linewidth}
\includegraphics[width=\linewidth]{fit_right.png}
\caption{Fit of $\ln(\text{Intensity})$ when the translatable arm was greater than equal path length}
\end{subfigure}%
\caption{Comparison of the linear fits for intensity as a distance from equal path length}
\end{figure}
Fringe visibility as a function of path length difference was measured on either side of equal path length, which was presumed to be between the 5th and 6th measurements. At $\tau-\tau_{0}<0$, the linear fit yields a slope (and equivalently Half Width at Half Maximum) of $0.578\pm \, 0.067ps^{-1}$ , which corresponds to an interaction time for pressure broadening of $\tau_{p} = 1.79 \pm 0.22$ ps.

At $\tau-\tau_{0}>0$, the linear fit yields a slope of $0.6\pm \, 0.14 \, ps^{-1}$ , which corresponds to an interaction time for pressure broadening of $\tau_{p} = 1.66 \pm 0.50$ ps. 


\begin{figure}
    \centering
    \includegraphics[width=0.5\linewidth]{pressurespectra.png}
    \caption{A depiction of the pressure broadened power spectrum of mercury with  each of the experimentally measured  $\tau_{p}$}
    \label{fig:Pressure Spectrum}
\end{figure}


\subsection{conclusion}
Fourier transform spectroscopy was used to measure the splitting of energy levels in Sodium due to spin orbit coupling, referred to as the sodium doublet. The doublet was measured to have a wavelength difference of $\Delta \lambda=0.58 \pm 0.0064$, in near agreement with previously recorded literature.  

The same technique was used to measure the effect of pressure broadening on the spectral emission of Mercury, following a Lorentzian distribution. Half width at half maximum of the distribution was measured to be $0.6 \pm 0.14 \times 10^{-12} $ Hz, corresponding to an interaction time $\tau_{p} = 1.79 \pm 0.22$ between mercury atoms in the light source. 


\section{sources of error}
Our micrometer is known to slip when changing directions. During the sodium experiment, we translated from the minimum to maximum distance, and then down - for a total of 5 traversals of the distance. This was done to minimize drift from changing the direction micrometer locally at each spot for 5 trials in a row. During the mercury experiment, the micrometer was left nearly in position but minorly corrected for movement between each recording of the visibility, which could lead to drift. Measurements were done on separate days, between which other students used the same experimental setup - therefore our estimate of equal path length is likely in the vicinity of, but not directly at, the reading for equal path length for the remainder of the mercury experiment.  

\begin{acknowledgments}
Thank you to Annika Larson, my lab Partner. Further thanks to Professors Theresa Lynn, Jason Gallicchio, and Sharon Gerbode.
\end{acknowledgments}

\begin{references}

\todo{ copy references from other report}

\end{references}

% ****** End of file stuff ******
\end{document}