# playlist-converter-lite
Convert an Apple Music playlist to a Spotify playlist

## Prerequisites
To use playlist-converter-lite, you must meet the following criteria:
- You have an Apple Developer account and a MusicKit API key.  [(More info)](https://developer.apple.com/documentation/applemusicapi/getting_keys_and_creating_tokens)
- You have a Spotify for Developers account and your app is properly registered.  [(More info)](https://developer.spotify.com/documentation/web-api/quick-start/)

## Getting Started
### Installation
```zsh
pip install playlistconverterlite
```

### Set Environment Variables
Set your app's Spotify Client ID and Client Secret as SPOTIPY_CLIENT_ID and SPOTIPY_CLIENT_SECRET environment variables.

On Mac:
```zsh
export SPOTIPY_CLIENT_ID=394jsd32jdj887377d783827dduw
export SPOTIPY_CLIENT_SECRET=60sjejjww998w8777399f9ds99
```

You will also need to set an environment variable SPOTIPY_REDIRECT_URI, which tells the Spotify API where to redirect the user once they have successfully entered their login info.

On Mac:
```zsh
export SPOTIPY_REDIRECT_URI=http://127.0.0.1:8080/
```

Also be sure to register the redirect URI in your app's settings on your Spotify Developer dashboard.

### Convert
```python
from playlistconverterlite import converter

new_playlist_link = converter.convert(
    pl_id="SOME_PLAYLIST",
    am_key="MY_KEY",
    am_kid="MY_KEY_ID",
    am_team_id="MY_TEAM_ID",
    sp_username="SPOTIFY_UN"
)
```

## License
https://github.com/andrewking1597/playlist-converter-lite/blob/main/LICENSE
