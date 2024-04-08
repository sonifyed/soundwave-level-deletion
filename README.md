# soundwave-level-deletion
A sonification method which deletes soundwave level data to represent time series data


Methods overflow (README for algorithm)
The indexing continues regardless if-statement comparisons. This means that if another zeroing out event occurs within the range of the gap_size parameter, then the resulting gap will be larger than the gap_size parameter.

Results Section Overflow
Gap_size parameter
Generally, we did not investigate how different gap_size parameters influence the perception of the work. However we wanted some evidence that we were justified in our design choice to insert a gap into the wave file rather than deleting individual frames. Participants of one focus group (Nov1) were played the Turandot piece with the gap_size parameter set to 4. As this is equal to the frame size for this wave file, this represents the output of the algorithm without the ‘zeroing out’ approach which we took to create interruptions. In a sense this creates a more accurate process, as the proportion of sample data will much more closely match the LPI value. However, this creates a very different sounding result. Participants stated that the sound “was very unpleasant to listen to. If I was in a museum, or that came on the radio or television, I would change the channel, or walk off. I wasn’t paying attention to the song; I was trying to mentally block out the fuzziness. It wasn’t pleasant at all”. Participants also reflected on how different this approach felt to the larger gap_size zeroing out approach, stating that that it “feels not like there’s something missing, but that there’s something wrong with the thing you are listening to.” They also described this approach as having “no missing pieces that you had in the first one (Turandot with gap_size=2400). […] [T]hose missing pieces give an impact that you don’t have in this disturbance (Turandot with gap_size=4), that is constant but the song is still fully there”. 
![image](https://github.com/sonifyed/soundwave-level-deletion/assets/62874711/8bbd31ce-0e9a-495c-8dad-64ffa6f6c7ec)
