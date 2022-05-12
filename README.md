# Bingo

> HTML5/JS bingo board game.

A easy to use bingo client written in vanilla HTML5/JQuery. Every 5x5 board is generated randomly on the user's device. The game is entirely local, and data is saved in local storage.

![Demo image](https://raw.githubusercontent.com/jacksonzamorano/bingo-app/master/sample.png)

## How to set up.

1. Fork or clone this repository.
2. Provide your game in `config.json` (see `Configuration` section below)
3. Serve statically
    1. This repo is already set up to run off Heroku's static buildpack (https://buildpack-registry.s3.amazonaws.com/buildpacks/heroku-community/static.tgz).
    2. However, any static server will do!

## Configuration

The default `config.json` contains a sample configuration. Override with your values as you please. You can add as many games to the array as you would like. The user can switch between them using the game switcher menu in the upper right.

### `Board` object

-   `key`: A unique key that identifies this game from different games. Make sure that there are no spaces. This key will be used to store local data in the browser.
-   `name`: The name the game will appear to the user as.
-   `middle_square`: The middle square that will always be pre-filled as free.
-   `options`: An array of strings. Each string is one potential square on the board. There needs to be at least 24 of these to play.

### Sample configuration

```
{
	"boards": [
		{
			"key":"example-bingo-game",
			"name": "Example Bingo Game",
			"middle_square": "Testing 123",
			"options": [
				"a",
				"b",
				"c",
				"d",
				... (etc)
			]
		}
	]
}
```
