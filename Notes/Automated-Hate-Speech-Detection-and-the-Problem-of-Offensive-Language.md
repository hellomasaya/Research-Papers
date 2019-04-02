### Objective:
 - Distinguish between hate-speech and offensive language
 - Classify tweets into three categories: hate-speech or offensive language or neither.
 - Train a model to differentiate between these categories and then analyze the results in order to better understand how can one distinguish between them.

### Challenges:
- People often use highly offensive terms but in a qualitatively different manner. Example - African Americans often use the term *n@gga* in every-day language online and people use terms like *h@e* and *b@tch* when quoting rap lyrics.
- Ambiguity. Example - the word gay can be used both pejoratively and in other contexts unrelated to hate speech.
- Non-linguistic features like the gender or ethnicity of the author can help improve hate speech classification but this information is often unavailable or unreliable on social media.
- 86% of the time the reason a tweet was categorized as racist was because it contained offensive words.
- Non-linguistic features like the gender or ethnicity of the author can help improve hate speech classification but this information is often unavailable or unreliable on social media 

### Dataset:
- A hate speech lexicon containing words and phrases identified by internet users as hate speech.
- Twitter API search - for tweets containing terms from the lexicon, resulting in a sample of tweets out of which a random sample of 25k tweets was taken to classify each of them into the three categories manually using this definition of hate speech: "language that is used to express hatred towards a targeted group or is intended to be derogatory, to humiliate, or to insult the members of the group."
- Result of manual coding: 5% - hate-speech and 76% offensive

### Training Model
- Tested a variety of models that have been used in prior work: logistic regression, naive Bayes, decision trees, random forests, and linear SVMs.
- Found that the Logistic Regression and Linear SVM tended to perform significantly better than other models. 
- Used a logistic regression with L2 regularization for the final model.

### Result:
- The best performing model gave an overall precision 0.91, recall of 0.90, and F1 score of 0.90.
- However, almost 40% of hate speech is misclassified - model is biased towards classifying tweets as less hateful or offensive than the human coders; the precision and recall scores for the hate class are 0.44 and 0.61 respectively.
