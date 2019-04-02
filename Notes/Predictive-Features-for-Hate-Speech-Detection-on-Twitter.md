### Objective and contribution:
- Provide a data set of 16k tweets annotated for hate speech.
- Classify tweets as racist or sexist or neither.
- Investigate which of the features used provide the best identification performance.
- Analyze the features that improve detection of hate speech in their corpus.

### Dataset:
- Performed an initial manual search of common slurs and terms used pertaining to religious, sexual, gender, and ethnic minorities.
- Identified a small number of prolific users from these searches.
- Used the public Twitter search API to collect the entire corpus - ensures that they obtain non-offensive tweets that contain both clearly offensive words and potentially offensive words, but remain non-offensive in their use and treatment of the words.
- Manually annotated data set, review annotations - an outside annotator.
- Identify hate speech with a clear decision list to ensure that problematic tweets are identified.
- Disagreement of annotations: due to context/ different opinion/definition of sexism.

### Demographic distribution:
- Identified 52% of the users in the annotated database.
- A large part of the perpetrators of hate speech in the dataset are men.

### Lexical distribution:
- Removed stop words, with the exception of “not”, special markers such as “RT” (Retweet) and screen names, and punctuation.
- Construct the ten most frequently occurring words by selecting the ten words with the most frequent occurrence for each class. 
- The terms frequently occurring in each class differ significantly.
- The most frequent tokens for racism are necessary in order to discuss Islam, while discussing women’s issues does not require the use of most of the terms that occur most frequently.
- Many of the tweets flagged as racist pertain to Judaism and Islam.

### Evaluation of influence of different features on prediction in a classification task:
- In order to pick the most suitable features, **a grid search over all possible feature set combinations** is performed, finding that using **character n-grams outperforms using word n-grams** due to character n-gram matrices being far less sparse than the word n-gram matrices.
- Using character n-grams of lengths up to 4, along with gender as an additional feature provides the best results.
- Using location or length is detrimental to the scores.
- Adding gender information improves score.
