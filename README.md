# Desktop Weather device (built on Balena)
Balena-fied version of the mustard corner desktop weather device.

You can [buy a kit here](https://mustardcorner.com/desktop-weather) or [build one yourself!](https://mustardcorner.com/desktop-weather). Go ahead and follow the [build guide](https://docs.google.com/document/d/11vR3yRZwERgpbvUFGCC37iavZzRNs2ug5QalcxWYfPg/edit?usp=sharing) for printing, soldering and wiring. When you hit the software step, that's where this repo steps in!

## Setup

### OpenWeather API key
1. Create an account [here](https://home.openweathermap.org/users/sign_up)
2. Go to “My API keys” from the top right menu:
    <p align="left"><img src="https://raw.githubusercontent.com/nucleardreamer/balena-desktop-weather/main/docs/api-key-screenshot.png"></p>
4. Generate a new API key using any name you like.
5. Ensure that the API key is activated and the status says “Active”.
6. Copy the Key as we will need this later. You will set the environment variable of `OPEN_WEATHER_APIKEY` with this key.
    Note: It takes about 10-15 minutes for the API key to start working and for us to have access.

### Configure environment variables
1. Head over to [http://desktop-weather.local/](http://desktop-weather.local/)
2. Navigate to the `Configuration` section
3. Click `Add/change Environment Variable`
4. Set your `OPEN_WEATHER_APIKEY` as the `key`, and your token from before as `value`
    <p align="left"><img src="https://raw.githubusercontent.com/nucleardreamer/balena-desktop-weather/main/docs/add-env-var.jpg"></p>
5. Set `LATITUDE` and `LONGITUDE` the same way, with your own values
    Note: If you don't see the variables showing up, it's possible the service has restarted - so go ahead and wait just a minute before trying again (this is normal behavior)

## Environment variables

| Environment variable | Type | Default | Description |
| --- | --- | --- | --- |
|`OPEN_WEATHER_APIKEY`|`String`|`not_set`|OpenWeather API key|
|`LATITUDE`|`Number`|`19.6069`|Set your latitude|
|`LONGITUDE`|`Number`|`-155.5056`|Set your longitude|
|`SERVO_PIN_1`|`Number`|`18`|Opional pin for first servo|
|`SERVO_PIN_2`|`Number`|`23`|Opional pin for second servo|
|`BUTTON_PIN`|`Number`|`17`|Optional pin for your push button|
---
