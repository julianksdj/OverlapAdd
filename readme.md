# Overlap-add (FFT passthrough)
 
 This plugin stores samples in an input buffer, when it has enough samples, it performs the FFT of FFT_SIZE input samples, then the IFFT of it and overlap-adds the result to a circular output buffer. For each audio frame samples from the circular output buffer are copied to the output circular buffer.
 
 The purpose of this project is to provide a template of a JUCE plugin to perform any operations in the frequency domain.
 Using this project the programmer can quickly embbed any frequency domain processing code inside the `processFFT` function.
 
 For the FFT and IFFT operations, fftw3 library is used. fftw3 binary and header files are included inside the project.
 
 FFTW is a C subroutine library for computing the discrete Fourier transform (DFT) in one or more dimensions, of arbitrary input size, and of both real and complex data. The FFTW package was developed at MIT by Matteo Frigo and Steven G. Johnson. More info: https://www.fftw.org/

 This video helped me understand the overlap-add operation: https://www.youtube.com/watch?v=xGmRaTaBNZA (I basically adapted the overlap-add code to JUCE). I recommend watching this video for great quality audio processing tutorials.
