# soundwave-level-deletion
A sonification method which deletes soundwave level data to represent time series data

**Software Versions**

This algorithm was written as a Jupyter notebook (v6.0.1) running Python (v3.7.4) and uses the wave (v0.0.2), numpy (v1.17.2), and pandas (v0.25.1) python packages.

**Inputs**

Input Audio File

Global.csv

**Setting the Gap_size parameter**

The gap_size parameter must be set to a multiple of the sample width multiplied by the number of channels of the input audio wave file. The smaller you set the gap_size parameter, the longer the algorithm will take to run. For all of our examples, we set the gap_size parameter to 2400.
We briefly investigated how different gap_size parameters influenced the perception of the work. We played one set of focus group participants an example of the output sonification of nessun dorma where the gap_size was equal to the frame_size, which was 4. Participants stated that the sound “was very unpleasant to listen to. If I was in a museum, or that came on the radio or television, I would change the channel, or walk off. I wasn’t paying attention to the song; I was trying to mentally block out the fuzziness. It wasn’t pleasant at all”. Participants  reflected on how different this approach felt to a larger gap_size, stating that that it “feels not like there’s something missing, but that there’s something wrong with the thing you are listening to.”
