The script is designed so that while running the collections will update once a day. If you want a collection to only update on specific days you can add the `schedule` attribute to it.

Below is an example of a collection with multiple schedules: 
```yaml
collections:
  TMDb Trending Weekly:
    tmdb_trending_weekly: 30
    sync_mode: sync
    schedule: weekly(sunday)
  TMDb Top Rated:
    tmdb_top_rated: 30
    sync_mode: sync
    schedule: monthly(1), monthly(15)
```

The scheduling options are:

| Name | Description | Format | Example |
| :--- | :--- | :--- | :--- |
| Hourly | Update this collection only when the script is run in that hour | hourly(Hour of Day) | hourly(17) |
| Daily | Update this collection once a day | daily | daily  |
| Weekly | Update this collection once a week on the specified day | weekly(Day of Week) | weekly(sunday) |
| Monthly | Update this collection once a month on the specified day | monthly(Day of Month) | monthly(1) |
| Yearly | Update this collection once a year on the specified day | yearly(MM/DD) | yearly(01/30) |
| Range | Updates this collection whenever the date is within the range | range(MM/DD-MM/DD) | range(12/01-12/31) |

* Using `daily` to schedule a collection is the default when `schedule` isn't specified
* You can run the script multiple times per day but using the `--time` command line argument detailed on the [Local Installation Page](https://github.com/meisnate12/Plex-Meta-Manager/wiki/Local-Installation#time-to-run).
* You can have multiple scheduling options just make them a list or comma-separated values
* You can use the `delete_not_scheduled` setting to delete Collections that are skipped due to not being scheduled.