# Etherpad Lite on Heroku

Forked from https://github.com/Pita/etherpad-lite and tweaked to run on Heroku's Cedar stack.

## Installation

``` console
$ git clone https://github.com/brighterplanet/etherpad-lite-heroku.git
Cloning into etherpad-lite-heroku...
$ cd etherpad-lite-heroku
$ heroku create my-very-own-etherpad --stack cedar
Creating my-very-own-etherpad... done, stack is cedar
$ heroku addons:add cleardb:ignite
----> Adding cleardb:ignite to my-very-own-etherpad... done, v2 (free)
$ heroku config:add ETHERPAD_KEY=AnythingYouWant
Adding config vars and restarting app... done, v3
$ git push heroku master
Counting objects: 6120, done.
$ heroku ps:scale web=1
Scaling web processes... done, now running 1
$ heroku open
Opening http://my-very-own-etherpad.herokuapp.com/
```

## Configuration
``` console
$ heroku config:add ETHERPAD_DEFAULT_TEXT="Hello world"
```

## License
[Apache License v2](http://www.apache.org/licenses/LICENSE-2.0.html)