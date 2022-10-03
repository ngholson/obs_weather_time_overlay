# Live weather and time overlay for OBS

<a href="https://github.com/ngholson/obs_weather_time_overlay/archive/refs/heads/main.zip">Download here</a>

**This requires a free account with OpenWeatherMap.org**
https://home.openweathermap.org/users/sign_up 

<B>NOTE: IT WILL TAKE 5-10 MINUTES FOR YOUR NEW API KEY TO WORK. PLEASE BE PATIENT.</b>

open the ```weatherWidget.html``` file with any text editor:<br>
 change the following:<br><br>
 ```yourApiKey``` Your OpenWeatherMap API key.<br>
 ```yourCity``` Your city name. <i>(example:"London, UK" or "Las Vegas, NV, US" or "Moscow")</i><br>
 ```yourUnits``` fahrenheit, celsius, kelvin see notes below. (```imperial```, ```metric```, ```standard```)<br>
 ```weatherDisplay``` options: ```full```, ```simple```, ```temp```, ```time``` (```temp``` and ```time``` only display temp or time)<br>
 ```weatherIcons``` turns on weather display icons: 1=on 0=off<br>
 ```iconHeight``` weather Icon height<br>
 ```textSize``` text size<br>
 ```textColor``` text color<br>
 ```displayWidth``` weather display width<br>

```
weatherWidget.html

var yourApiKey = "CHANGE_ME";		// your OpenWeatherMap Api key here
var yourCity = "CHANGE_ME";		// your city name, ex: "London, UK" or "Las Vegas, NV, US" 
var yourUnits = "imperial";		// 'imperial' for fahrenheit  'metric' for celsius  'standard' for kelvin.
var weatherDisplay = "full";		// options: "full" , "simple" , "temp" , "time"
var weatherIcons = 1;			// show Weather status icons in display 1=on  0=off
var iconHeight = "12px";		// weather icon height in px
var textSize = "10pt";			// font size
var textColor = "black";		// font color
var displayWidth = "400px";		// weather display box width

```

Save the file and open OBS-Studio

in OBS, add a new "browser" source to the scene you want to dispaly the weather and time. 
change the URL for the source the path to the ```weatherWidget.html``` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.

