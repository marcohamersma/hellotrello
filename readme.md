# HelloTrello

This bot checks a Trello board periodically and sends notifications of card creations and comments to an IRC chatroom. It works with multiple teams/chatrooms and can optionally ping a scrum master or team lead as a notification. It's built with Ruby and the [Cinch](https://github.com/cinchrb/cinch) framework.

## Setup
-  Generate an API key at [trello.com/1/appKey](https://trello.com/1/appKey/generate)
-  Make a copy of `config.example.yml` and rename it `config.yml`
-  Request a token via: `https://trello.com/1/authorize?key=APIKEY&name=HelloTrello&expiration=never&response_type=token`
-  Add the token and API key, Trello board id and an optional scrum master to `config.yaml`
  - Multiple boards per team are allowed, just make the board ID an array
-  Run `bundle install`
-  Run it (by typing `ruby hellotrello.rb` for example)
-  Profit

## Commands
- `hellotrello help` : Will display a small text of possible commands.
- `hellotrello getme 123`: Will retrieve a description and link for that card.
- `hellotrello quit` : quits the bot

### Todos
-  Better modularisation
-  Use proper Ruby logging, not puts
-  Add a procfile
-  Print board name when teams have multiple boards
-  Make new ticket by title and get a link and number in return

### could dos
-  Dynamic polling intervals based upon board activity / time of day
-  Elegant solution for when multiple teams follow one board
