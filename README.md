# hassio_rowing_game
Boat game for Home Assistant

## Screenshots
![Alt text](/screenshots/1.png?raw=true "1")
![Alt text](/screenshots/2.png?raw=true "2")

## Intention
For my rowing machine, which supports FTMS (https://github.com/dudanov/hassio-ftms) to have a nice dashboard for the gathered informations.
Just starring on those statistics werent enough, so I created a game inside HA.

This is not just applicable to a rowing machine. But basically every "input".

## Installation
I cracked up my yaml-configuration files for HA in different parts, so it is easier to manage them.
You find the base in "configuration.yaml".
Just paste the rest of the yaml-files inside your ones, based on your needs.

The boats, that are shown are in the "www"-directory.

The dashboard you can just paste as "Raw cofiguration"-yaml.

In the "templates.yaml", set the sensor, which is used as your user input. Currently it is "sensor.user_boat_progress".

## Usage
* Set the rowing distance of "sensor.rowing_distance" via the dashboard.
* Opponent 1 and 2 are configured as values ranging from 0.5-2. Where 0.5 is the easiest, 2 is very hard.
They are a bit esotheric, as they randomly add a value.
* Opponent 3 and 4 is defined as seconds per 500 meter. So when you define "rowing_distance" of 2000 meter, and 1 minute for opponent 3 for 500 meter, it is done in 4 minutes.
