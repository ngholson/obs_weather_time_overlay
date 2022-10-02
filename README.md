# obs_weather_time_overlay
Weather and Time overlay widget for OBS


**This requires a free account with OpenWeatherMap.org**
https://home.openweathermap.org/users/sign_up 
 
 Once you have your openweathermap account and free API key you will need to make the following changes in the weatherWidget.html file.<br>
 <B>NOTE: IT WILL TAKE 5-10 MINUTES FOR YOUR NEW API KEY TO WORK. PLEASE BE PATIENT.</b>
 
 open the ```weatherWidget.html``` file with any text editor:<br>
 change the following:<br><br>
 ```yourApiKey``` Your API key.<br>
 ```yourCity``` Your city name. <i>(example:"London, UK" or "Las Vegas, NV, US" or "Moscow")</i><br>
 ```yourUnits``` fahrenheit, celsius, kelvin see notes below. (imperial, metric, standard)

```
//********************************************************************************************************************************
// CHANGE THESE SETTINGS 

var yourApiKey = "CHANGE_ME";	  // your OpenWeatherMap Api key here
var yourCity = "CHANGE_ME";	  // city name, ex: "London, UK" or "Las Vegas, NV, US"
var yourUnits = "imperial";       // 'imperial' for fahrenheit  'metric' for celsius  'standard' for kelvin.

</script>

<!-- Weather Display CSS change as needed -->
<style> 
body {
	background: rgba(0,0,0,0);	/* removes body background */
}

.weather-box {                    /* weather display CSS */
	border: 1px solid #000;   /* BORDER SIZE AND COLOR */
	border-radius:5px;        /* ROUNDED CORNERS */
	background: lightgrey;    /* WEATHER DISPLAY BACKGROUND COLOR */
	text-align:center;        /* TEXT ALIGNMENT */
	font-family:tahoma;       /* FONT */
	font-size:10pt;           /* FONT SIZE */
	font-weight:bold;         /* FONT WEIGHT */
	color: black;             /* FONT COLOR */
	width: 500px;		  /* WEATHER DISPLAY WIDTH */
}

</style>	
<!--
//********************************************************************************************************************************
// NO CHANGES BELOW HERE
//********************************************************************************************************************************
```

Save the file and head over to OBS-Studio

in OBS add a new "browser" source to the scene you want to dispaly the weather and time. 
change the URL for the source the path to the ```weatherWidget.html``` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.

