# Live weather and time overlay for OBS


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
weatherWidget.html

//************************************************************************************************************************
// CHANGE THESE SETTINGS 

var yourApiKey = "CHANGE_ME";		// your OpenWeatherMap Api key here
var yourCity = "CHANGE_ME";		// your city name, ex: "London, UK" or "Las Vegas, NV, US" 
var yourUnits = "imperial";		// 'imperial' for fahrenheit  'metric' for celsius  'standard' for kelvin.

//************************************************************************************************************************
</script><style> 
/* ---------------------------------------------  CSS OPTIONS START HERE  ----------------------------------------------*/
body {
	background: rgba(0,0,0,0);	/* removes body background		(transparent background do not change)	*/
	}
.weather-box {				/* weather display CSS			(start of weather box css)		*/
	border: 1px solid #000;		/* BORDER SIZE AND COLOR		(size style color)			*/
	border-radius:5px;		/* ROUNDED CORNERS			(corder radius in pixels)		*/
	background: lightgrey;		/* WEATHER DISPLAY BACKGROUND COLOR	(can be web friendly name, hex, rgba)	*/
	text-align:center;		/* TEXT ALIGNMENT			(center, right, left, justify)		*/
	font-family:tahoma;		/* FONT					(what web friendly font to use)		*/
	font-size:10pt;			/* FONT SIZE				(how big is the font)			*/
	font-weight:bold;		/* FONT WEIGHT				(bold, bolder, normal)			*/
	color: black;			/* FONT COLOR				(can be web friendly name, hex, rgba)	*/
	widtH: 400px;			/* WEATHER DISPLAY WIDTH		(width of weather box)			*/
	}

/* ---------------------------------------------  NO CHANGES BELOW HERE  -----------------------------------------------*/
```

Save the file and head over to OBS-Studio

in OBS add a new "browser" source to the scene you want to dispaly the weather and time. 
change the URL for the source the path to the ```weatherWidget.html``` file you just saved.
change the height and width to 1920x1080.

save and position as needed.

REMEMBER: IT WILL TAKE 5-10 MINUTES FOR YOUR API KEY TO BECOME ACTIVE. THIS WILL NOT WORK UNTIL IT DOES.

