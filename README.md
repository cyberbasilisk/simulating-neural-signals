# simulating-neural-signals
Python implementation of various neural signal simulation methods.

Simulating data is an important part of neural signal processing. When neural data is simulated, the ground truth / empirical features of the simulated signal are known. This allows the verification of research and processing methods. This is achieved by comparing the known ground truth to the results obtained from these processing methods, enabling the fine tuning and validation of these methods before application on real data.

Neural signals are in the form of a time series data. They conventionally have a 3 dimensional shape, that is, Channels by Time Points by Trials, in no particular order. Simulated data should inherit this shape. That being said, there are a variety of ways to simulate neural data.

[Sinewaves](simulating-neural-signals/sinewaves.ipynb) demonstrates the simulation of neural data by generating sine waves and adding random noise. Since the ground truth is known, that is the frequency and amplitude of the sine waves in this case, it can be used to validate processing methods such as the extraction of the Static Power as shown in [Sinewaves](simulating-neural-signals/sinewaves.ipynb).
