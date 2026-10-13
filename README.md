Project Description: Real-Time Musical Note Extraction Using an STM32 Microcontroller

This project aims to develop an embedded digital signal processing (DSP) system capable of extracting and identifying musical notes from an audio signal using an STM32 microcontroller. The system analyzes a melody, detects individual notes, estimates their fundamental frequencies, and converts them into their corresponding musical note names.

The implemented algorithm follows several DSP stages:

Audio Acquisition

An audio recording of a melody (e.g., Beethoven's Für Elise) is loaded and processed.
A specific time window containing musical notes is selected for analysis.

Signal Preprocessing

The audio signal is downsampled using a moving average filter to reduce computational complexity.
This operation preserves the essential characteristics of the signal while making it suitable for embedded implementation on an STM32 platform.

Note Detection

A dynamic thresholding technique is applied to detect the onset of musical notes.
The threshold is continuously adjusted based on the local signal amplitude, allowing the algorithm to distinguish notes from background noise.

Frequency Extraction

Each detected note segment is isolated.
The Fast Fourier Transform (FFT) is performed to determine the dominant frequency component of the note.
The fundamental frequency is identified from the FFT spectrum.

Note Identification

The extracted frequencies are mapped to standard musical notes (A, B, C, D, E, F, G and their sharps/flats).
This enables automatic transcription of the melody into a sequence of musical notes.

Melody Reconstruction

Using the detected note frequencies, the melody is regenerated through sinusoidal signal synthesis.
The reconstructed audio is played back and stored as a new audio file for comparison with the original melody.
Objectives
Apply Digital Signal Processing (DSP) techniques on an STM32 microcontroller.
Implement efficient note detection and frequency estimation algorithms.
Demonstrate real-time audio analysis capabilities on an embedded system.
Explore practical applications such as music transcription, digital tuners, and intelligent musical instruments.
Technologies and Methods
STM32 Microcontroller
MATLAB for algorithm development and validation
Fast Fourier Transform (FFT)
Digital Filtering and Downsampling
Adaptive Thresholding
Frequency-to-Note Conversion
Audio Signal Processing
Expected Results

The system successfully detects the individual notes of a melody, identifies their frequencies, converts them into musical notation, and reconstructs the original song with a high level of accuracy. The final implementation demonstrates the feasibility of performing musical note recognition in real time on a resource-constrained STM32 embedded platform.
