This quickstart will get you going with [deck.js](http://imakewebthings.com/deck.js/) and includes the [remote deck.js](https://github.com/chrisjaure/deckjs-remote) functionality

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

#What is it?

[Deck.js](http://imakewebthings.com/deck.js/) is a framework to make HTML based presentations.  One of it's extensions [remote deck.js](https://github.com/chrisjaure/deckjs-remote) allows a presenter to control the current slide that all of the connected guests are viewing.

For example, if you installed this to your heroku account and navigated to http://my-app-name.herokuapp.com/example/?master and the person you were presenting to navigated to http://my-app-name.herokuapp.com/example/ you would be presented with this:

![Password Prompt](https://raw.githubusercontent.com/pcon/heroku-deckjs-remote-quickstart/master/docs/deck_step1.png)

After the presenter enters the password (the default being "master"), the guest will be prompted to join the session

![Session Prompt](https://raw.githubusercontent.com/pcon/heroku-deckjs-remote-quickstart/master/docs/deck_step2.png)

Once the guest has joined the session, any slide changes that the presenter makes will be conveyed to the guest

![Presentation](https://raw.githubusercontent.com/pcon/heroku-deckjs-remote-quickstart/master/docs/deck_step3.png)

#How do I install it?

## Running on Heroku

Create an account at [http://heroku.com](http://heroku.com)

Click this button
[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Adding new presentations

Copy the contents of `public/example/` to a new location and edit the `index.html` file.  Then commit and repush to view.

## Remote controlling a presentation

1. Navigate to the presentation and add `?master` to the URL
2. Type in the password of _master_
3. Wait until your guests have loaded the presentation and selected _Join_
4. Give your presentation

## Changing the default password

1. Generate a new md5sum with your new password `printf "mynewpassword" | md5sum `
2. Take the hash and edit `public/extensions/remote/deckjs-remote.js` and change the hash in `key = '...'`
