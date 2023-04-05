# Bio_Medical_EMG_Assignment

## Matlab-based EMG Pre-Processing:
For this exercise, I wrote Matlab code to preprocess an EMG signal. The code first filtered the signal using a band pass filter with a range of 30-450 Hz. To recover the phase delay, I used the 'filtfilt' function. Then, I rectified the signal and computed the envelope of the muscle signals using a low pass filter with a range of 3-6 Hz. Finally, I downsampled the signal. The code generated a figure with three panels, which showed:
* The EMG raw signal with the filtered signal plotted on top in a different color
* The EMG rectified signal with the envelope plotted on top in a different color
* The movement signals with the envelope plotted on top

## Simulink-based EMG Control:
For this exercise, I used Simulink to control a cursor on a screen based on EMG signals. The Simulink model read the EMG data from a mat file and mapped the signals to cursor movements. To reach the targets in the 4 cardinal directions, I mapped each muscle to a specific direction (e.g. one muscle to go up, another down, etc.) and set a threshold for each muscle to determine when the target had been reached. I was able to successfully control the cursor to reach the 4 cardinal direction targets.

To reach the other 4 targets displayed on the screen, I would need to map the remaining muscles to these directions.

## Limitation
One drawback of this approach is that it requires mapping each muscle to a specific direction, which can become complicated when working with a large number of muscles or more complex movements.

## Future Improvements
For a different way of mapping the EMG activity to the control of the cursor, I could use machine learning algorithms to train the system to recognize patterns in the EMG signals and translate them into specific movements of the cursor. However, this approach would require a large amount of training data and would be more complex to implement.
