# SentimentAnalysis
Utilizing transfer learning in the form of a ULMFiT language model and an LSTM (with additional weight dropout) to predict tweet sentiment data. 

The sentiment140 dataset can be found here: https://www.kaggle.com/kazanova/sentiment140

The following excel formula can be used to clean the dataset of handle mentions, where F1 represents the cell containing the string to be processed. 

=TEXTJOIN(" ",1,IF(LEFT(TRIM(MID(SUBSTITUTE(F1," ",REPT(" ",LEN(F1))),(ROW(INDIRECT("1:"&LEN(F1))))*LEN(F1)-(LEN(F1)-1),LEN(F1))),1)="@","",TRIM(MID(SUBSTITUTE(F1," ",REPT(" ",LEN(F1))),(ROW(INDIRECT("1:"&LEN(F1))))*LEN(F1)-(LEN(F1)-1),LEN(F1)))))
