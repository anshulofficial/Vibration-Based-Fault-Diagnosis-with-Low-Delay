# Vibration-Based Fault Diagnosis with Low Delay



The system delay $\tau_d$ of a vibration-based condition monitoring system can be defined as ***the time the system takes to acquire input vibration segment and classify or predict the operational condition of the current state of the equipment***. In vibration-based monitoring, the current state $S_c$ is represented by the input segment $v_{in}$ of the generated vibration signal as shown in the figure below. Accordingly, the system delay is the sum of the time duration of input segment $T_{v_{in}}$ and the online processing time $T_p$ .


<p float>
<img src="https://github.com/Western-OC2-Lab/Vibration-Based-Fault-Diagnosis-with-Low-Delay/blob/main/Figure_01.png"/>
</p>


<ul>
<li>The time duration of the input segment depends on number of data points in the segment.
<li>The online processing time is algorithm-dependent; it involves two tasks, feature extraction (including pre-processing) and condition prediction/classification. <br>
</ul>
Hence, online processing time can be generally viewed as a function of the number of data points in the input segment, the size of extracted features, and available computing resources. Thus, designing a condition monitoring system with low system delay involves three main requirements: <br>

<ol>
  <li>Extracting features of high sensitivity to fault-related transients to improve system accuracy.</li>
  <li>Extracting features of small size.</li>
  <li>Utilizing input vibration segments of relatively short time duration or equivalently, of small number of data points.</li>
</ol>

Accordingly, the paper utilizes wavelet decomposition and Fourier analysis, and proposes a hybrid method to fulfill the aforementioned requirements and extract a small number of highly discriminative features from short-duration vibration signals. The first step involves decomposing the input vibration segment using $k$-level Wavelet Packet Transform (WPT). Consequently, $2^k$ elementary waveforms of lower and higher frequency sub-bands are reconstructed from individual wavelet coefficients.
In the second step, Fast Fourier Transform (FFT) is applied to the resultant waveforms to obtain the spectral contents of each waveform. Hence, a
feature vector of size $S=1×(m×2^k)$ can be reconstructed by utilizing the first $m$ dominant frequency components in the spectrum of each waveform as illustrated in the figure below.<bR>

<p>
<img src="https://github.com/Western-OC2-Lab/Vibration-Based-Fault-Diagnosis-with-Low-Delay/blob/main/Figure_02.png"/>
</p>



## Codes and Datasets:

A separate Jupyter notebook is provided for each of the three datasets. Functions for processing .mat vibration files and creating training/testing datasets are included in the notebooks as well.<br>

### Datasets:<br>
[the Case Western Reserve University (CWRU) bearing dataset](https://engineering.case.edu/bearingdatacenter)<br>
[the Paderborn University (PU) bearing dataset](https://mb.uni-paderborn.de/en/kat/main-research/datacenter/bearing-datacenter/data-sets-and-download)<br>
[the University of Ottawa (uOttawa) bearing dataset](https://data.mendeley.com/datasets/v43hmbwxpm/2)<br>





## Contact Information
For all inquiries or collaboration opportunities please contact: <br>

Email : anshulyadav0fficial07@gmail.com <br>
Github: [anshulofficial](https://github.com/anshulofficialhttps://github.com/anshulofficial) <br>




