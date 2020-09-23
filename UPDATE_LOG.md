## Updates
The new Twitoff application that uses the SpaCy library to vectorize tweets instead of Basilica. 
* Predict.py:
  * (line 20) - embed user given tweet through vectorize_tweet function found in twitter.py
* Twitter.py:
  * Deleted Basilica authentication
  * (line 40) - embeds all the tweets when new user is added 
* Deleted Cache feature