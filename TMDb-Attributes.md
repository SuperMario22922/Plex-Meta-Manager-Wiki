Configuring [TheMovieDb](https://www.themoviedb.org/) is required in order to run the script. 

A `tmdb` mapping is in the root of the config file.

Below is a `tmdb` mapping example and the full set of attributes:
```yaml
tmdb:
  apikey: ################################
  language: en
```

| Name            | Attribute  | Allowed Values       | Default |      Required      |
|:----------------|:-----------|:---------------------|:-------:|:------------------:|
| TMDb V3 API Key | `apikey`   | User TMDb V3 API Key |   N/A   | :heavy_check_mark: |
| Language        | `language` | User Language        |   en    |        :x:         |

If you do not have a TMDb V3 API key please refer to this [guide](https://developers.themoviedb.org/3/getting-started/introduction).
