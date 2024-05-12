<H3>ENTER YOUR NAME : Aruru Sai Bandhavi</H3>
<H3>ENTER YOUR REGISTER NO : 212221240006</H3>
<H3>DATE:12.05.2024</H3>
<H1 Align="center">Project Based Experiment<H1>

### Objective:

Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.
  
### Program:
```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)

```
### Output: 

![image](https://github.com/Saibandhavi75/Project-Based-Experiment-AAI/assets/94208895/7a7a3bc9-1fc3-489a-8b22-4b5f1563372d)
![image](https://github.com/Saibandhavi75/Project-Based-Experiment-AAI/assets/94208895/46e41ff1-c850-4c47-b4b6-2cb22a99018b)



### Inference:
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
