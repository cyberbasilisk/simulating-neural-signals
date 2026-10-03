# simulating-neural-signals
Python implementation of various neural signal simulation methods.

Simulating data is an important part of neural signal processing. When neural / EEG data is simulated, the ground truth / empirical features of the simulated signal are known. This allows the verification of research and processing methods. This is achieved by comparing the known ground truth to the results obtained from these processing methods, enabling the fine tuning and validation of these methods before application on real data.

Neural signals are in the form of a time series data. They conventionally have a 3 dimensional shape, that is, Channels by Time Points by Trials, in no particular order. Simulated data should inherit this shape. In the absence of any one of these dimensions, we assume their shape is 1. That being said, there are a variety of ways to simulate neural data.

[sinewaves](sinewaves.ipynb) demonstrates the simulation of neural data by generating sine waves and adding random noise. Since the ground truth is known, that is the frequency and amplitude of the sine waves in this case, it can be used to validate processing methods such as the extraction of the Static Power as shown in [sinewaves](sinewaves.ipynb).

Another way of simulating Neural data is by generating ‘Chirps’. A Chirp is a frequency modulated sine wave. Basically, this is a single sine wave with multiple frequencies, either increasing or decreasing. Demonstrated in [chirps](chirps.ipynb).

Morlet Wavelets can also be used in neural data simulation. These wavelets are narrow band and transient. These features are exhibited by real EEG data. This is demonstrated in [transient](transient.ipynb).

Electrodes enable the measurement of brain activity. So far, we have been simulating data at the electrode level, hence simulating electrode measurements. In dipoles, we're going to simulate the sources of brain activity which project to the scalp, and are picked up or measured by these electrodes. In short, we are going to be simulating the projections of neurons onto the scalp. 
