# Digital-Signal-Processing

## Sounds and Signals
#### Exercise 1.1:
Go to Freesound and download a sound sample that includes music, speech, or other
sounds with a well-defined pitch. Every student should have a unique chosen sound sample
compared to others. Students with the same chosen sound sample will be considered cheating.They will automatically be given a grade of 0 for this laboratory activity. Select a roughly half-
second segment where the pitch is constant. Compute and plot the Spectrum of the segment you selected. What connection can you make between the timbre of the sound and the harmonic
structure you see in the Spectrum? Use high_pass, low_pass, and band_stop to filter out some harmonics. Then, convert the Spectrum back to a wave and listen to it. How does the sound relate to the changes you made in the Spectrum?

#### Exercise 1.2
Synthesize a compound signal by creating Sine_Signal and Cos_Signal objects and
adding them up. Evaluate the signal to get a Wave and listen to it. Compute its Spectrum and
plot it. What happens if you add frequency components that are not multiples of the
fundamental?

#### Exercise 1.3
Write a function called stretch that takes a Wave and a stretch factor and speeds up or
slows down the wave by modifying ts and framerate.
Hint: It should only take two lines of code.

## Harmonics

#### Exercise 2.1:
A sawtooth signal has a waveform that ramps up linearly from -1 to 1, then drops to -1
and repeats. (See http://en.wikipedia.org/wiki/Sawtooth_wave)
Write a class called SawtoothSignal that extends Signal and provides evaluate to
evaluate a sawtooth signal..
Compute the spectrum of a sawtooth wave. How does the harmonic structure compare
to triangle and square waves?

#### Exercise 2.2:
Make a square signal at 1100 Hz and make a wave that samples it at 10000 frames per
second. If you plot the spectrum, you can see that most of the harmonics are aliased. When you
listen to the wave, can you hear the aliased harmonics?

#### Exercise 2.3:
If you have a spectrum object, spectrum, and print the first few values of spectrum.fs,
you’ll see that they start at zero. So spectrum.hs[0] is the magnitude of the component with
frequency 0. But what does that mean?
Kindly try this experiment listed below:
* Make a triangle signal with frequency 440 Hz and make a Wave with duration 0.01 seconds.
Plot the waveform.
*  Make a Spectrum object and print spectrum.hs[0]. What is the amplitude and phase of this
component?
*  Set spectrum.hs[0] = 100. Make a Wave from the modified Spectrum and plot it. What
effect does this operation have on the waveform?

#### Exercise 2.4:
Write a function that takes a Spectrum as a parameter and modifies it by dividing each
element of hs by the corresponding frequency from fs.
Hint: since division by zero is undefined, you might want to set spectrum.hs[0] = 0.
Test your function using a square, triangle, or sawtooth wave.
*  Compute the Spectrum and plot it.
*  Modify the Spectrum using your function and plot it again.
*  Make a Wave from the modified Spectrum and listen to it. What effect does this operation
have on the signal?

#### Exercise 2.5:
Triangle and square waves have odd harmonics only; the sawtooth wave has both even
and odd harmonics. The harmonics of the square and sawtooth waves drop off in proportion to
1/f; the harmonics of the triangle wave drop off like 1/f2 . Can you find a waveform that has even and odd harmonics that drop off like 1/f2?

> Hint: There are two ways you could approach this: you could construct the signal you
want by adding up sinusoids, or you could start with a signal that is similar to what you want
and modify it.
