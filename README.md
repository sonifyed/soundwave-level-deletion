# soundwave-level-deletion
A sonification method which deletes soundwave level data to represent time series data.

**Software Versions**

This algorithm was written as a Jupyter notebook (v6.0.1) running Python (v3.7.4) and uses the wave (v0.0.2), numpy (v1.17.2), and pandas (v0.25.1) python packages.

**Running Jupyter Notebooks**

Please use this advice in downloading and running the Jupyter Notebook: https://www.codecademy.com/article/how-to-use-jupyter-notebooks



The algorithm is divided into three cells. The first cell imports the packages necessary to run the algorithm. The second cell contains most things that the user may edit: input data as .csv, df_data_column_title, input audio file as .wav, gap_size parameter, the number_of_segments, and the name of the output .wav file. The third cell contains all the rest of the algorithm. The three cells must be run in order for the algorithm to work. On repeat runs in the same session, it is not necessary to run the first cell. 

**Input data**

The algorithm takes a comma separated values file (.csv) as input. The data must be time series data ranging between 0 and 1 inclusive. The example data 'Global.csv' uses Living Planet Index data from 1970 to 2018.

LPI 2022. Living Planet Index
database. 2022. < www.livingplanetindex.org/>. Downloaded on 29 November 2022


**df_data_column_title**

The algorithm reads the time series data by the title of the dataframe column, which is currently set to 'LPI_final' for the example LPI data in 'Global.csv'. If using your own data, ensure that this identifies the right column of data.

**Input audio file**

The algorithm requires a wave file (.wav) audio input file. For our example we have used 'mother-nature.wav', a public domain voice recording of the Emily Dickinson poem 'Mother Nature' recorded for Librivox.org by Jason Mills (https://archive.org/details/mothernature_1306_librivox/mothernature_dickinson_jcm.mp3). Another example wav file is provided, for nessun-dorma.wav, which is an open source (Public Domain Mark 1.0) recording of an aria from the opera Turandot by Giacomo Puccini, sung by Antonio Cortis in 1929 (https://archive.org/details/antonio-cortis-giacomo-puccini-turandot-nessun-dorma-gramophone-da-1075). However this example is larger so is provided as a zipped file which must be uncompressed before use.

**Gap_size parameter**

The gap_size parameter must be set to a multiple of the sample width multiplied by the number of channels of the input audio wave file. The smaller you set the gap_size parameter, the longer the algorithm will take to run. For all of our examples, we set the gap_size parameter to 2400. Decreasing the gap_size parameter will increase the runtime of the algorithm. 

Via our focus groups, we briefly investigated how different gap_size parameters influenced the perception of the work. We played one set of focus group participants an example of the output sonification of nessun dorma where the gap_size was equal to the frame_size, which was 4. Participants stated that the sound “was very unpleasant to listen to. If I was in a museum, or that came on the radio or television, I would change the channel, or walk off. I wasn’t paying attention to the song; I was trying to mentally block out the fuzziness. It wasn’t pleasant at all”. Participants  reflected on how different this approach felt to a larger gap_size, stating that that it “feels not like there’s something missing, but that there’s something wrong with the thing you are listening to.”

**Number of segments**

This should be equal to the number of time series data points that you have. Our data is yearly from 1970 to 2018, so we have set this to 49.

**Output audio file**

You need to give the title of your output audio wave (.wav) file. Ours is set to 'output-wave-file-name.wav'. It is essential that the flag 'wb' is here as this means that the 'wav file you create is writable.

**Instructions to reproduce 'My Way' Frank Sinatra example**
1. Source a copy of Frank Sinatra's hit song 'My Way' as a wave file (.wav.).
2. Save the file in tge same folder as the soundwave-level-deletion-algorithm.ipynb algorithm file.
3. Open the jupyter notebook https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html
4. Change the input .wav file name to match the name of your .wav file of 'My Way'. You may also want to change the name of the output.
5. Run all three code chunks in order.

