# Updates
The new Twitoff application that uses the SpaCy library to vectorize tweets instead of Basilica. 
>[SpaCy Documentation](https://spacy.io/usage/vectors-similarity)

* Predict.py:
  * (line 20) - embed user given tweet through vectorize_tweet function found in twitter.py that uses SpaCy word2vect
* Twitter.py:
  * Deleted Basilica authentication
  * (line 40) - embeds all the tweets when new user is added 
  * imported the en_core_web_sm
* .env:
  * No longer need Basilica authentication
* No longer need to import Basilica
* Deleted Cache feature

## IMPORTANT

### PIPENV:
* `<pipenv install spacy>`
* `<pipenv install https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-2.2.0/en_core_web_sm-2.2.0.tar.gz#egg=en_core_web_sm>`
> This downloads the model and lets Heroku find it in our Pipfile (small model: sm, medium model: md, large model: lg)
* `<pipenv uninstall basilica>`

### OTHER:
* Upon installation of Spacy be sure to download the [model](https://spacy.io/usage) as well.
> Students will need this as well. You can also use ...md or ...lg but more accurate with large models
`<python -m spacy download en_core_web_sm>`
* On production you also need to include a requirments.txt to communicate the download of this en_core_web_md
```text
<spacy>=2.2.0,<3.0.0
https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-2.2.0/en_core_web_sm-2.2.0.tar.gz#egg=en_core_web_sm
```
> You can also download the tar file directly and access it through your requirements through the following (what I did, your choice)
```text
./en_core_web_sm-2.2.5.tar.gz
```

### Notes: 
* Runs slower than the Basilica API (suprising I know) but just keep that in mind when adding new users. 
* need to import the actual model `<import en_core_web_sm>` and then load it `<nlp = en_core_web_sm.load()>`
> You can also access it indirectly through the first bullet point in **OTHER** through `<nlp = spacy.load(en_core_web_sm)>`

## Deploying

