# module_14_challenge

For SVM when the window size changes the total accuracy will stay relatively the same of 55% but the values of percision, recall, and f1-score will change. I ran 3 test one with a significant increase from 100 to 360 for long and 10 for short, in this case the f1 score increase for the -1 signal by .01 which is insignificant much like this score the other catergories had minute changes. When I increased the short window to 20 and long to 200 the accuarcy was still 55 but the recall for -1 was higher went from .07 to .22 also recall increase by .11 percision had a slight increase. The Final product was an extreme small window 2 and 25. In this window set accuarcy dropped by 1% and the numbers moved slightly but nothing was drastic. It looks like the best window I used was 20 and 200 due to higher recall and f1-score.

output.png


## Using ADA Boost
The original Dataset had a lower accuarcy rating then SVM the rating was 52%. We see the numbers tended to be more tight together between 1 and -1, in SVM the spread was quite large. In using the best window we had for SVM 20 and 200 our accuarcy has dropped by 4% which is now at 50%. One thing to note on this is the first inverse for 1 and -1 the Recall for -1 is higher than 1. With putting short to 10 and long to 360 we do see accuarcy going up to 52%, and with increasing the spread of the window to 2 short and 500 long accuracy has greatly dropped to 45%. One final test is to make this model have a tight window to see if that would help, and with having 25 and 100 accuracy only went to 52%.
precision    recall  f1-score   support

        -1.0       0.44      0.32      0.37      1793
         1.0       0.56      0.68      0.61      2284

    accuracy                           0.52      4077
   macro avg       0.50      0.50      0.49      4077
weighted avg       0.51      0.52      0.51      4077

## Original Data numbers
4/ 100
precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

## Increase in Window for Both Short(20) and Long(200)

precision    recall  f1-score   support

        -1.0       0.46      0.15      0.22      1740
         1.0       0.57      0.87      0.68      2227

    accuracy                           0.55      3967
   macro avg       0.51      0.51      0.45      3967
weighted avg       0.52      0.55      0.48      3967

precision    recall  f1-score   support

        -1.0       0.41      0.13      0.19      1828
         1.0       0.56      0.86      0.67      2324

    accuracy                           0.54      4152
   macro avg       0.48      0.49      0.43      4152
weighted avg       0.49      0.54      0.46      4152

Total accuarcy stays the same but we see a big dip in F1 score for -1