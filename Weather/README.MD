# Weather Module Information

The weather module uses the Open Weather Map API (https://openweathermap.org/api) 

You must sign up for a free account with Open Weather Map and generate an API key to use this module. 


## Configuration

Using the Configuration utility, enable the weather module and paste your Open Weather Map API key into the appropriate field (image here)

Specify a latitude and longitude for your location. (find them using https://www.latlong.net) (image here)

Please note that it can take up to a few hours for your Open Weather Map API key to become active, so if it doesn't work right away, that's normal.

## Controlling from EOS

You can also turn the module on/off using OSC

`/weather/set/status=true` or `/weather/set/status=false` will enable/disable the module. 
		
- EDC reponds with `/weather/out/set/status=true (or false)`

`/weather/set/api=apikeyhere` will set your API key

- EDC reponds with `/weather/out/set/api=apikeyhere`

`/weather/set/lat=1.352` and `/weather/set/lon=35.191` will set the lat and lon of your position. These must be sent as separate messages.

- EDC reponds with `/weather/out/set/lat=1.325` or `/weather/out/set/lon=35.191`

`/weather/set/units=imperial` will set the units of your responses (metric or imperial)

- EDC reponds with `/weather/out/set/units=imperial` 

`/weather/set/forecast/hourly=8` will set the total number of hourly forecasts you want (0 for none, up to 8 for +8 hours in the future)

- EDC reponds with `/weather/out/set/forecast/hourly=8` 

`/weather/set/forecast/daily=5` will set the total number of hourly forecasts you want (0 for none, up to 5 for +5 days in the future)

- EDC reponds with `/weather/out/set/forecast/daily=5` 

### Setting the refresh rate

The weather module sends you new forecasts every 15 minutes unless you disable it.

`/weather/get/current=yes` will send current weather report, regardless of enable/disable status. (only once)

## Data you will recieve

`/weather/out/current/date="Monday, August 2nd 2024"`

`/weather/out/current/temp=80.2°`

`/weather/out/current/temp/high=90.2°`

`/weather/out/current/temp/low=70.2°`

`/weather/out/current/feelslike=84.1°`

`/weather/out/current/pressure=1020`

`/weather/out/current/dewpoint=64.13`

`/weather/out/current/humidity=43`

`/weather/out/current/uvindex=9.99`

`/weather/out/current/windspeed=3.4`

`/weather/out/current/windbearing=0`

`/weather/out/current/visibility=1000`

`/weather/out/current/weather="Partly cloudy"`

`/weather/out/current/rainchance="40%"`

### Sunrise/Sunset

`/weather/out/today/sunrise="06:00:00"`

`/weather/out/today/sunset="20:04:00"`

### Hourly Forecast

You can get up to 8 hours of future forecast - just change the `/next/1/` to `/next/2/` up to `/next/8/` for example. You must set up how many you want in your initial connection to EOS (See above)

`/weather/out/forecast/hourly/next/1/hour=15:00` (returns the name of the next hour)

`/weather/out/forecast/hourly/next/1/temp=81.2°`

`/weather/out/forecast/hourly/next/1/weather="Partly cloudy"`

`/weather/out/forecast/hourly/next/1/rainchance="60%"`

### Daily Forecast

You can get up to 5 days of future forecast - just change the `/next/1/` to `/next/2/` up to `/next/5/` for example. You must set up how many you want in your initial connection to EOS (See above)

`/weather/out/forecast/daily/next/1/date="Tuesday"` (returns the name of the next day)

`/weather/out/forecast/daily/next/1/temp/high=81.2°`

`/weather/out/forecast/daily/next/1/temp/low=69.2°`

`/weather/out/forecast/daily/next/1/weather="Partly cloudy"`

`/weather/out/forecast/daily/next/1/rainchance=60%`



