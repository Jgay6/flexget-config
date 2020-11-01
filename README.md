# [Flexget](http://www.flexget.com) Configuration Files

The configuration has tuned to my personal preference, but could be useful for beginner
or to adapt to your personal preference.

## Workflow
- Looks for watchlist from different inputs sites, for movies/series
from Trakt (Looking for and libre/open source alternative),
for anime use myanimelist/kitsu/anidb (I still can't decide which is better)
- Add those movies/series in different list depending of the type
- For movies add those to and special Spanish movies with english names and Spanish names
- Search movies/series in different discover sites, usually torrent site,
for Spanish movies and anime with custom rename and blacklist, for example for Spanish movies only allow Spanish dubbing movies,
and for anime just Japanese dubbing
- Add movies/series/anime to different [transmission](https://transmissionbt.com/) instance, one in my home server and other to my VPS
- Send notification to XMPP/Telegram when the download start
- Copy complete movies/series/anime to their respective folder depending of the type,
to something like `/net/shared/Movies/Spanish`, `/net/shared/Movies/General` or `/net/shared/Movies/Anime`
- Look for duplicate movies/series/anime and delete it after approval, Send notification to XMPP when found duplications.
- Remove movies with rating lower then 5 after approval, Send notification to XMPP about that.

## Configuration structure
```
 - config.yml // main flexget configuration
 - variables.yml // accounts/secrets/paths and everything that can be shared between tasks
 - series.yml // custom hardcoded TV series
 - anime.yml // custom hardcoded TV anime series
```

## Installation
1. Install [Flexget](http://www.flexget.com)
2. Clone this repository into the `.flexget` directory of your home directory.
3. Rename `variables.yml.sample` to `variables.yml` and setup the accounts/directories
4. Rename `series.yml.sample` and `anime.yml.sample` to `series.yml`, `anime.yml`
4. Run Flexget as daemon
    ```bash
    flexget daemon start -d
    ```

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png "License CC0")](http://creativecommons.org/publicdomain/zero/1.0/)
