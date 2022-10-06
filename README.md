# Live weather and time overlay for OBS
screenshot:<br>
<center>
<img src="https://obsproject.com/forum/attachments/screen_shot-png.87338/"></center>

### <a href="https://github.com/ngholson/obs_weather_time_overlay/archive/refs/heads/main.zip">Download here</a>

**This requires a <a href="https://home.openweathermap.org/users/sign_up">free API key</a> from OpenWeatherMap.org**

<B>NOTE: IT WILL TAKE 5-10 MINUTES FOR YOUR NEW API KEY TO BECOME ACTIVE. PLEASE BE PATIENT.</b>

open the ```weatherWidget.html``` file with any text editor:<br>
 change the following:<br><br>
 <b><i>Required:</b></i><br>
 ```yourApiKey``` Your OpenWeatherMap API key.<br>
 ```yourCity``` Your city name. <i>(example:</i>```London, UK``` <i>or</i> ```Las Vegas, NV, US``` <i>or</i> ```Moscow```<i>)</i><br>
 ```yourUnits``` fahrenheit, celsius, kelvin see notes below. (```imperial```, ```metric```, ```standard```)<br>
 
 <b><i>Optional:</b></i><br>
 ```weatherDisplay``` options: ```full```, ```weather```, ```simple```, ```temp```, ```time``` (```temp``` and ```time``` only display temp or time)<br>
 ```weatherIcons``` turns on weather display icons: ```1```=on ```0```=off<br>
 ```iconHeight``` weather Icon height<br>
 ```textSize``` text size<br>
 ```textColor``` text color<br>
 ```displayWidth``` weather display width<br>
 ```weatherBackground``` weather box color (if ```dynamicBackground``` is enabled, this will only apply during the day hours)<br>
 ```dynamicBackground``` weather box will change based on day/night. ```1```=on ```0```=off<br>
 ```clockSeperator``` optional: seperator for the temp and time in full mode only (ex: ```-```, ```/```, ```.```, ```*```, additional spaces, etc.)<br>
 <br>
```
weatherWidget.html

var yourApiKey = "CHANGE_ME";		// your OpenWeatherMap Api key here
var yourCity = "CHANGE_ME";		// your city name, ex: "London, UK" or "Las Vegas, NV, US" 
var yourUnits = "imperial";		// 'imperial' for fahrenheit  'metric' for celsius  'standard' for kelvin.
var weatherDisplay = "full";		// options: "full" , "weather", "simple" , "temp" , "time" (default = "full")
var weatherIcons = 1;			// show Weather status icons in display 1=on  0=off
var iconHeight = "22px";		// weather icon height in px
var textSize = "20pt";			// font size
var textColor = "black";		// font color
var displayWidth = "850px";		// weather display box width
var weatherBackground = "lightgrey";    // weather Background color  (if dynamicBackground is enabled this only applies during daytime hours)
var dynamicBackground = 1;              // weather background changes based on day or night 1=on 0=off
var clockseperator = "";	        // optional: seperator for the temp and time in full mode only (ex: -, /, ., *, additional spaces, etc.)

```

Save the file and open OBS-Studio

in OBS, add a new "browser" source to the scene you want to dispaly the weather and time. 
change the URL for the source the path to the ```weatherWidget.html``` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.
<center>
<img src="https://obsproject.com/forum/attachments/screen_shot-png.87338/">
</center>
