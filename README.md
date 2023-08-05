# Yahoo Fantasy Sports Data Query

This Python script uses the `yfpy` package to query Yahoo Fantasy Sports data. The script is set up to authenticate with Yahoo Fantasy Sports, set up several variables for desired data, configure the query, and execute a number of potential queries.

## Installation

To use this script, you will need to have Python installed on your machine. The script also uses the following libraries:
- os
- pathlib
- dotenv
- yfpy
- json

You can install the non-standard libraries using pip from the terminal:
```
pip3 install python-dotenv yfpy
```

## Usage

Before running the script, you need to create an .env file in the same directory as your script and add the following lines:

```
YFPY_CONSUMER_KEY=your_consumer_key
YFPY_CONSUMER_SECRET=your_consumer_secret
```

Replace 'your_consumer_key' and 'your_consumer_secret' with your actual Yahoo Fantasy Sports consumer key and secret.

In the script, you can modify the following variables to specify the data you want to retrieve:

- season: the desired season year
- chosen_week: the desired week
- game_code: the desired Yahoo Fantasy Sports game code
- game_id: the desired Yahoo Fantasy Sports game ID
- game_key: the desired Yahoo Fantasy Sports game key
- league_id: the desired league ID
- team_id: the desired team ID 
- player_id: the desired player ID
- league_player_limit: the maximum number players you wish the get_league_players query to retrieve

The script is currently set up to call the get_current_league_standings function, which retrieves the current league standings and saves them to a JSON file in a 'data' directory within the directory specified by auth_dir. You can uncomment any of the other yahoo_query method calls to retrieve other data to the console.

To run the script, navigate to the directory containing the script in your command line and run the following command:
```
python3 script.py
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
