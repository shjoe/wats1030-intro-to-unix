# Stretch Goals for the *nix Scavenger Hunt

The following goals are meant to provide a way for more experienced users to
extend their knowledge of the *nix command line.

* Use `curl` to look up the URL `https://www.imdb.com/title/tt0070948/`. The title of this film will lead you to the answer. *What is the answer?*

```
I used: 
$ curl -L https://www.imdb.com/title/tt0070948/ | grep '<title>'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0        <title>Zardoz (1974) - IMDb</title>
100 34976    0 34976    0  <title>TryIMDbProFree</title>

The title is Zardoz (1974)
```
