# Updates
The new Twitoff application that uses the SpaCy library to vectorize tweets instead of Basilica. 
>[SpaCy Documentation](https://spacy.io/usage/vectors-similarity)

* Predict.py:
  * (line 20) - embed user given tweet through vectorize_tweet function found in twitter.py that uses SpaCy word2vect
* Twitter.py:
  * Deleted Basilica authentication
  * (line 40) - embeds all the tweets when new user is added 
* Deleted Cache feature
* .env:
  * No longer need Basilica authentication

## IMPORTANT

### PIPENV:
* `<pipenv install spacy>`
* `<pipenv uninstall basilica>`

### OTHER:
* Upon installation of Spacy be sure to download the [model](https://spacy.io/usage) as well.
> Students will need this as well
`<python -m spacy download en_core_web_md>`

