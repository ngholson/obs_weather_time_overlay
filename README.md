# Live weather and time overlay for OBS

screenshot:<br>

<center>
<img src="./preview.png"></center>

# <a href="https://github.com/ngholson/obs_weather_time_overlay/archive/refs/heads/main.zip">Download here</a>

**This requires a <a href="https://home.openweathermap.org/users/sign_up">free API key</a> from OpenWeatherMap.org**<br><i>make sure you sign up for the free api key under the "<b>professional collections</b>" section and <b>NOT</b> the "One Call by Call" or the API 3.0 subscription plan.</i>

Multi-Language Support. Reads default language information from browser (in this case OBS) and displays output in that language.

<B>NOTE: IT WILL TAKE 5-10 MINUTES FOR YOUR NEW API KEY TO BECOME ACTIVE. PLEASE BE PATIENT.</b>

After you have downloaded and extracted the .zip file, open the `weatherWidget.html` file with any text editor<br> and change the following variables:<br><br>
<b><i>Required:</b></i><br>
`yourApiKey` Your OpenWeatherMap API key.<br>
`yourCity` Your city name. <i>(example:</i>`London, UK` <i>or</i> `Las Vegas, NV, US` <i>or</i> `Kiev`<i>)</i><br>
`yourUnits` fahrenheit, celsius, kelvin. (`imperial`, `metric`, `standard`)<br>

<b><i>Optional:</b></i><br>
`weatherDisplay` options: `full`, `weather`, `simple`, `temp`, `time` (`temp` and `time` only display temp or time)<br>
`weatherIcons` turns on weather display icons: `1`=on `0`=off<br>
`iconPack` set which icons to use. (1-3) (add your own, see the text file in the images folder.)<br>
`iconHeight` weather Icon height (for best results use textSize + 2. ex: textSize = 20pt + 2 = 22px)<br>
`textSize` text size<br>
`textColor` text color<br>
`weatherBackground` weather box color (if `dynamicBackground` is enabled, this will only apply during the day hours)<br>
`dynamicBackground` weather box will change based on day/night. `1`=on `0`=off<br>
`clockSeperator` optional: seperator for the temp and time in full mode only (ex: `-`, `/`, `.`, `*`, blank spaces, etc.)<br>
`time24hour` if enabled time is displayed in 24hr format vs 12hr format<br>
`weatherBorder` border size around weather display<br>
`autoCheckUpdates` if enabled overlay will check for updates when first loads.<br>

<br>
Save the file and open OBS-Studio

in OBS, add a new "browser" source to the scene you want to dispaly the weather and time.
change the URL for the source to the path of the `weatherWidget.html` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

<b>KNOWN ISSUE:</b><br>
If your town shares a name with another town, for instance Long Beach, CA and Long Beach, MS. The larger area can use just the short format variable "long beach", in fact in some cases <i>must</i> use the short format, but the smaller city/town would need to use the long format "long beach, ms, usa". <br><br>

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.

<center>
<img src="./preview.png">
</center>
