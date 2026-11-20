# SMS Spam Classifier

## What it does
Takes a text message and predicts whether it's spam or not.

## Data
SMS Spam Collection dataset: 5,572 messages (4,825 ham, 747 spam).

## Approach
- Converted text to numbers with TF-IDF and CountVectorizer
- Trained a Multinomial Naive Bayes classifier
- Split 80/20 into train/test

## Results
| Vectorizer | Accuracy | Spam Precision | Spam Recall |
|---|---|---|---|
| TF-IDF | 96.7% | 1.00 | 0.75 |
| CountVectorizer | 99% | 0.94 | 0.95 |

## What I learned
- high accuracy doesn't mean a good model, we also need to check the other measurments like recall,
   precision, F-score it will tell us how good our model performs.
- The approach depends on the thing we expect, in the experiments the CountVectorizer
   let fewer spam messages reached the user but the downside was that it also flagged normals mails as spam  
- Training data size matters a lot. With only 50 messages, the model predicted
  "ham" for everything: 87% accuracy, but did not caught spam. It learned nothing
  useful because it had too few spam examples.
