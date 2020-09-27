# Updates
The new Twitoff application that uses the SpaCy library to vectorize tweets instead of Basilica. 
>[SpaCy Documentation](https://spacy.io/usage/vectors-similarity)

* Predict.py:
  * (line 20) - embed user given tweet through vectorize_tweet function found in twitter.py that uses SpaCy word2vect
* Twitter.py:
  * Deleted Basilica authentication
  * (line 40) - embeds all the tweets when new user is added 
* .env:
  * No longer need Basilica authentication
* No longer need to import Basilica
* Deleted Cache features

## IMPORTANT

### PIPENV:
* `<pipenv install spacy>`
* `<pipenv uninstall basilica>`

### OTHER:
* Upon installation of Spacy be sure to download the [model](https://spacy.io/usage) as well.
> Students will need this as well. You can also use ...md or ...lg but more accurate with large models
`<python -m spacy download en_core_web_sm>`

### Notes: 
* need to import the actual model `<import en_core_web_sm>` and then store it in a directory in the base git repo.
``` python

```

## Deploying

