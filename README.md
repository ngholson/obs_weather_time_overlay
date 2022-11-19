# Live weather and time overlay for OBS

screenshot:<br>
<center>
<img src="https://obsproject.com/forum/attachments/screen_shot-png.87338/"></center>

# <a href="https://github.com/ngholson/obs_weather_time_overlay/archive/refs/heads/main.zip">Download here</a> 

**This requires a <a href="https://home.openweathermap.org/users/sign_up">free API key</a> from OpenWeatherMap.org**<br><i>make sure you sign up for the free api key under the "professional collections" section and not the "One Call by Call" subscription plan.</i>

Multi-Language Support. Reads default language information from browser (in this case OBS) and displays output in that language.

<B>NOTE: IT WILL TAKE 5-10 MINUTES FOR YOUR NEW API KEY TO BECOME ACTIVE. PLEASE BE PATIENT.</b>

open the ```weatherWidget.html``` file with any text editor:<br>
 change the following:<br><br>
 <b><i>Required:</b></i><br>
 ```yourApiKey``` Your OpenWeatherMap API key.<br>
 ```yourCity``` Your city name. <i>(example:</i>```London, UK``` <i>or</i> ```Las Vegas, NV, US``` <i>or</i> ```Kiev```<i>)</i><br>
 ```yourUnits``` fahrenheit, celsius, kelvin. (```imperial```, ```metric```, ```standard```)<br>
 
 <b><i>Optional:</b></i><br>
 ```weatherDisplay``` options: ```full```, ```weather```, ```simple```, ```temp```, ```time``` (```temp``` and ```time``` only display temp or time)<br>
 ```weatherIcons``` turns on weather display icons: ```1```=on ```0```=off<br>
 ```iconPack``` set which icons to use. (1-3) (add your own, see the text file in the images folder.)<br>
 ```iconHeight``` weather Icon height (for best results use textSize + 2. ex: textSize = 20pt + 2 = 22px)<br>
 ```textSize``` text size<br>
 ```textColor``` text color<br>
 ```weatherBackground``` weather box color (if ```dynamicBackground``` is enabled, this will only apply during the day hours)<br>
 ```dynamicBackground``` weather box will change based on day/night. ```1```=on ```0```=off<br>
 ```clockSeperator``` optional: seperator for the temp and time in full mode only (ex: ```-```, ```/```, ```.```, ```*```, blank spaces, etc.)<br>
 ```time24hour``` if enabled time is displayed in 24hr format vs 12hr format<br>
	```weatherBorder``` border size around weather display<br>
	```autoCheckUpdates``` if enabled overlay will check for updates when first loads.<br>
 <br>
```
weatherWidget.html

// REQUIRED
var yourApiKey = "CHANGE_ME";        // your OpenWeatherMap Api key here
var yourCity = "CHANGE_ME";          // your city name, ex: "London, UK" or "Las Vegas, NV, US" or "Kiev"
var yourUnits = "imperial";          // 'imperial' for fahrenheit  'metric' for celsius  'standard' for kelvin.

// OPTIONAL
var weatherDisplay = "full";         // options: "full" , "weather", "simple" , "temp" , "time" (if blank or error, default is "full")
var weatherIcons = 1;                // show Weather status icons in display 1=on  0=off
var iconPack = 3;                    // Icon Pack ID. (1-3) (add your own just follow the folder (pack1, pack2, pack3...) and file (01d.png, 01n.png) naming convention.  
var iconHeight = "22px";             // weather icon height (for best results use textSize + 2. ex: textSize = 20pt + 2 = 22px)
var textSize = "20pt";               // font size
var textColor = "black";             // font color
var weatherBackground = "lightgrey"; // weather Background color  (if dynamicBackground is enabled this only applies during daytime hours)
var dynamicBackground = 1;           // weather background changes based on day or night 1=on 0=off
var clockSeperator = "";             // optional: seperator for the temp and time in full mode only (ex: -, /, ., *, @, additional spaces, etc.)
var time24hour = false;              // 24 hour time.  true or false
var weatherBorder = "0";             // border size in pixels. default is 0
var autoCheckUpdates = true;         // Automatically check for updates.
```
<br><br>
Save the file and open OBS-Studio

in OBS, add a new "browser" source to the scene you want to dispaly the weather and time. 
change the URL for the source the path to the ```weatherWidget.html``` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

<b>KNOWN ISSUE:</b><br>
If your town shares a name with another town, for instance Long Beach, CA and Long Beach, MS. The larger area can use just the short format variable "long beach", in fact in some cases <i>must</i> use the short format, but the smaller city/town would need to use the long format "long beach, ms, usa". <br><br>

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.
<center>
<img src="https://obsproject.com/forum/attachments/screen_shot-png.87338/">
</center>
