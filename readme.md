# HelloTrello

This bot checks a Trello board periodically and sends notifications of card creations and comments to an IRC chatroom. It works with multiple teams/chatrooms and can optionally ping a scrum master or team lead as a notification. It's built with Ruby and the [Cinch](https://github.com/cinchrb/cinch) framework.

## Setup
-  Generate an API key at [trello.com/1/appKey](https://trello.com/1/appKey/generate)
-  Request a token via: `https://trello.com/1/authorize?key=substitutewithyourapplicationkey&name=My+Application&expiration=never&response_type=token`
-  Add the token and API key, Trello board id and an optional scrum master to `config.yaml`
  - Multiple boards per team are allowed, just make the board ID an array
-  Run `bundle install`
-  Run it (by typing `ruby hellotrello.rb` for example)
-  Profit

## Commands
- `hellotrello help` : Will display a small text of possible commands.
- `hellotrello getme 123`: Will retrieve a description and link for that card.

### Todos
-  Make new ticket by title and get a link and number in return
