First, we need to find the frequency that is emitted from our microwave sources. To do this, we rely on standing waves. 

## Finding Frequency:
### Theory
We emit a microwave between two plates. An incoming wave will pass through the first one and partly reflect off the second. The reflected wave will either constructively or destructively interfere, depending on the phase of the wave. The distance between the each maximum constructive interference is the half the emitted wavelength. We measure the distance between 10 constructive interferences, which is 5 * the wavelength. We use this to find the frequency emitted by our equipment, given by $c=\lambda \nu$, where $c$ is the speed of light, $\lambda$ is the wavelength, and $\nu$ is the frequency. 

### Experiment to find the frequency of our emitters
We take two trials where for each we measure the distance between 10 constructive interference nodes. This is measured by using a receiver behind the reflecting plate, and finding the maximum power read on it's scale, then watching and counting 10 consecutive minimums and maximums that occur while moving our transmitter continuously further away. 

The calibration yielded Table 1 Data. We found an estimate of 12.46 $\pm 3$  GHz emitted by our microwave emitter.   

## Finding the receiving characteristics of our receiver

We want to check if our receiver yields a value from the intensity or the received electric field strength or 

### Theory
We will rotate the angle of the emitted electromagnetic wave relative the the receiver. Since they are both linearly polarized, only the component of the field that is parallel to the receiver will be detected. This way, we can find if the receiver is measuring strength or intensity of the electric field. We would predict the intensity to drop by $\cos ^{2}\theta$, whereas if it is by field strength it would change by $\cos(\theta)$.

## Finding the characteristic of our receiver:
We set our receiver to 10 x sensitivity, and adjusted such that 0 degrees (near perfect alignment) would have a maximum current of $1$ mA.  We then rotated our receiver in increments of 15 degrees and found the received current. We plot this against both $\cos$ and $\cos ^{2}$. It appears to be most linear with $\cos ^{2}$, so the receiver appears to measure the intensity. See Table 2 for data.


Table 1:

|                         |          |                    |          |          |
| ----------------------- | -------- | ------------------ | -------- | -------- |
|                         |          |                    |          |          |
|                         | Trial 1  |                    | Trial 2  |          |
| 5 periods               | 11.4     | Error              | 12.75    | Error    |
| 1 wavelength            | 2.28     | 0.05 cm            | 2.55     | 0.05 cm  |
| Frequency (Hz)          | 1.32E+10 | 3e9 Hz             | 1.18E+10 | 3e9 Hz   |
| Frequency (GHz)         | 13.16    | 3 GHz              | 11.76    | +/-3 GHz |
|                         |          |                    |          |          |
| Average found frequency |          | Average wavelength |          |          |
| 12.46                   | GHz      | 2.415              | cm       |          |
|                         |          |                    |          |          |


Table 2:

|                   |                       |                  |
| ----------------- | --------------------- | ---------------- |
| Receiver Response |                       |                  |
| theta (degrees)   | Receiver reading (mA) | Uncertainty (mA) |
| 0                 | 1.00                  | 0.05             |
| 15                | 0.95                  | 0.05             |
| 30                | 0.78                  | 0.05             |
| 45                | 0.55                  | 0.05             |
| 60                | 0.30                  | 0.05             |
| 75                | 0.07                  | 0.05             |
| 90                | 0.00                  | 0.05             |

See Figures 1, 2, and 3 for the comparisons with $\cos$and $\cos ^{2}$.
