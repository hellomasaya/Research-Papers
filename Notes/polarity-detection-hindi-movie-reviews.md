## Intoduction
### Three levels of sentiment analysis:
  - Document level: polarity of the whole doc.
  - Sentence level: polarity of sentence.
  - Aspect level: polarity of sentence/document for each feature it contains.
  
### Challenges in Hindi sentiment analysis
  - Free word order in sentences in Hindi.
  - Same words having same meaning occur in multiple context.
  - Sufficient resources not available.
 
### Existing work: TLDR
 
## Approach: 
Created a hindi dictionary with synonyms-antonyms; handles negation - to determine polarity.
### Preprocessing of data:
  - POS tagging to determine feature and opinion words.
  - Seed list - most frequent words with polarity.
  - Find opinion words(from after POS tagging) in seed list, if a word is not found in seed list, its synonyms are looked for  and if they match a word from seed list the opinion word along with its synonyms are stored in seed list

### Polarity detection:
   - The polarity of the reviews is determined on the basis of majority of opinion words, if positive words are more in the review than the polarity of the review is positive otherwise it is negative.
   - Negation handling - if the opinion word is followed by not then the polarity of review is reversed.
