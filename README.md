# doh-reh-mih
A simple algorithm that simulates a perceptron that adjusts  it learning rate to try predicting low tone from other tones.
The Praat software was used to record monosyllabic words with the high, mid and low tones across all the vowels of the Yoruba language.
The fundamental frequency (F0) was used as a distinguishing feature to classify HIGH, MID AND LOW TONES.
Therefore the pitch listing for each monosyllabic sounds were extracted to an excel spreadsheet, the pitch existed as a distribution of data(F0_Hz) across time.
The best way to represent this data is to draw a regression line to represent the means of this data distribution simultaneously.
The slope and the intercept for each distribution (pitch listing) was calculated using the excel function.
The slope and intercept was used as the features to which labels were assigned.
The excel spreadsheet was further modified to easily filter by tones (high, mid and low)
Since the algorithm tested for the low tone (the concept of OTR - One Versus The Rest) was used. Slope and Intercept for LOW TONES were labelled 1, the rest were labelled 0.
The features (slope and intercept) and label was extracted from the excel spreadsheet to a notepad and read into python with the pandas library as a pandas dataframe.
The dataframe was further processed by the perceptron-simulation algorithm where weights were assigned to each features, weights were further adjusted by the learning rate which was also adjusted per 1000 iteration.
The model classified low tones from the other tones with +80% accuracy on the 9,998 iteration with a learning rate of 0.20
