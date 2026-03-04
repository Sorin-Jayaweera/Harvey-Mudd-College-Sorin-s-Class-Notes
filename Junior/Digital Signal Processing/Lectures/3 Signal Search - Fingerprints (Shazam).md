
We want to find a query squiggle out of music and want to find that segment of music in a database of longer songs. 
![[Pasted image 20260203100109.png|300]]

We extract fingerprints from each song and store it in our database. We then search with the recorded data's fingerprints among the database. 

The key components are extracting fingerprints from a signal, assembling a database, and searching.
## Fingerprints

On audio, we calculate the Short Time Fourier Transform.

To find peaks, we divide the STFT matrix (S) into rectangular regions. In each region, we look for the peak energy (candidate peaks). We then make a region centered around each of those peaks, and check that it is the strongest within a region centered around it (an actual local maximum). 

We then pair the peaks. If there are two peaks, $m_{j},m_{i}$ that are within $\Delta_{\text{ max }}$ forwards in time, then we call them a "pair". Each point can have any number of peak pairs. For every peak, we consider all peaks within $\Delta_{\text{ max }}$ in front of it. $\Delta_{\text{ max }}$ is a "hyperparameter", which you can experiment with to find optimal. 

We then store these tuples of pairs in a single 32 bit integer. We have 10 bits for the frequency bin $k$ of the first, and 10 bits for the second. We also store the time difference between then (but instead of exact number of frames, we look at roughly how many frames). I.e. if they are 24 frames apart, we could bin them by how many "quantizations" apart, i.e. if $\Delta_{\text{ quant }}=4$, we would store to $\text{ floor }\left(\frac{24}{4}\right)$.

We are only using 26 bits, not 32 (???)
## Construct database
Lets make a reverse index. Lets make a column of finger print values, and for each fingerprint lets store which song had that fingerprint, as well as what frame number that finger print occurred. There can be multiple instances of a fingerprint in one song, and there can be many songs with the same fingerprints. This is saying "give me a list of all the songs that have this fingerprint". 



![[Pasted image 20260203103536.png]]


## Search

Lets consider a single fingerprint. We plot on the y axis the frames that that fingerprint lands on, and the x axis the times that that fingerprint exists in the song. 

If the song doesn't match, the times will not be correlated between the $x$ and $y$ axis. 

If the songs DO match, the slope would be 1 because the times of the frames would be correlated - the same weird spacings. The intercept would be random, but the slope would be 1. 
![[Pasted image 20260203104818.png]]

If we ASSUME that it is good, the time differences would be constant between each point. We can make a histogram of offsets, and it should be tight. We could have a huge spike of pairs that all fall at the offset between them.  We calculate a "match score", where the score is the max of the histogram counts. 

We then pick the song with the highest match score. 


