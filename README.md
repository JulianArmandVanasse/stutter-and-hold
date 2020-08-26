# Stutter+Hold
A timbral tremolo based on the phase vocodeur. The spectral freeze effect to prolong the tones of a single frame is extended through _Stutter+Hold_ to update the held frame at a regular interval. 

## Hear It
To audition the plug-in and its use cases, watch (and listen) to the following video:

[![Sounds that'll make you curious!](https://img.youtube.com/vi/dxMSjbI3etM/0.jpg)](http://www.youtube.com/watch?v=dxMSjbI3etM)

## Under the Hood
The interface has been designed so that any interested party can add the plug-in to their library and get started immediately with this novel effect, regardless of prior knowledge of audio processing. But, for interested parties this section outlines the tools at play and some innovations by the developers.

### Phase Vocodeur
Essential to this effect is a framework for making local estimates of frequency content in the signal and modifying the signal based on these estimates. The estimation process is known in DSP literature as the _Analysis_ stage, and the modification process as the _Synthesis_ stage.  The Short-Time Fourier Transform (STFT), Wavelets and the elusive Matching Pursuit are various techniques for implementing this two stage process, but the most common technique used in real-time audio signal processing is the use of the STFT. An alternative name is the [Phase Vocodeur](https://cycling74.com/tutorials/the-phase-vocoder-%E2%80%93-part-i), and linked here to a great introduction to this process in the Max/MSP environment. 

To estimate the frequency over a short interval, the signal is divided into overlapping buffers and transformed into the frequency domain using the Fourier transform (FT). Once in the 

### Timbral Tremolo

#### Envelope Following

#### Basilar Compression


## Behind the Curtain
_Stutter+Hold_ is developed by Max Henry and Julian Vanasse for the AES Student Competition: MATLAB Plugin. Prior to starting this project both had not yet programmed a real-time time-frequency processing system from the ground up and this competition served as a pretext for developing such a tool. For interested parties the developers will soon release the ```AnalysisSynthesis``` framework they built for spectral processing. 