# fufufilms

Python script that utilizes the tmdbsimple, omdb, and SendGrid (optional) APIs to return a list of highly-rated films (top rated, in-theaters, popular, etc).

"Highly-rated" is interpreted as an IMDB rating >= 7.5 (out of 10) and a Metacritic rating >= 75 (out of 100).

First off, get your FREE API keys:

- For TMDBSimple, go to https://www.themoviedb.org/
- For OMDB, go to http://www.omdbapi.com/
- For SendGrid, go to https://sendgrid.com/

Set up your Python environment; acquire the necessary Python packages

- pip install tmdbsimple
- pip install omdb
- pip install sendgrid

Input your newly acquired API key values into "creds.py".

Feel free to edit line #19 of "FufuFilms.py" for specialized movie lists.
By default, movies that are currently in theaters will be returned and evaluated.
For example, one can also use "response = tmdb_movies.top_rated()", to work from a list of already highly-rated film.

[OPTIONAL]
I created a process in Windows Task Scheduler that runs "FufuFilms.py" twice a month.
This bimonthly task is the reason I implemented a SendGrid function to send the final films list to target email addresses (spamming my friends :).

ENJOY! and tweak to your liking!