# [Stop Words](https://en.wikipedia.org/wiki/Stop_words) for [Jamaican Patois](https://en.wikipedia.org/wiki/Jamaican_Patois).

Here's a python package containing some commonly used words in Patois.

(Very unscientifically gathered)


## Usage

You can install it from pip: `$ pip install patois-stop-words` 

```python
from patois_stop_words import get_patois_stop_words

get_patois_stop_words()
```

Or just download `words.txt`if you prefer. 

### English and Patois 

Realistically, people usually use a mixture of English and Patois words in speech and informal writing (for example on Twitter).
You can solve for this by using stop words from Patois and English:

```
$ pip install stop-words patois-stop-words
```

```python
from patois_stop_words import get_patois_stop_words
from stop_words import get_stop_words

english_stop_words = get_stop_words('en')
patois_stop_words = get_patois_stop_words()

stop_words = english_stop_words + patois_stop_words

# Alternatively, if you're using nltk:

from nltk.corpus import stopwords

stop_words = stopwords.words('english') + patois_stop_words
```

Please let me know if you decide to use this in some way! 

Based on [python-stop-words](https://github.com/Alir3z4/python-stop-words)
