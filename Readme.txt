Hi Andreas,
 
I don’t have a WGT for the webinos connected car demo. I have created a zip-file containing all the relevant data.
The content of the zip file needs to be copied into the web_root folder. The demo works on webinos 0.8. The demo should be executed using firefox.
 
Here are steps to get everything running:
 
1.     Change settings in ‘webinos_config.json’
Set the connector parameter for the Vehicle and Geolocation API to ‘simulator’. In this case you can change properties of the Vehicle and the Geolocation using localhost:9898/simulator/vehicle.html
2.     Create the  ‘travel’ folder inside  the ‘default’ folder of the Webinos-Platform.
In this folder the updates files of  travel plans are stored using the File API.
3.     Change the behavior of the backspace key in firefox to handle backspace as ‘go back a page in the session history’ (only on linux). This can be changed using about:config. The relevant parameter is ‘browser.backspace_action’ and the value needs to be ‘0’. This change is relevant, if you want to demonstrate the applications using only keys.  The relevant keys to control the automotive view of the applications are the following:
a.     TAB: focus the next element (focusing the next element in a list)
b.     TAB+SHIFT: focus the previous element
c.     ENTER: Select an element
d.    ESC: Opens the app switcher between  ‘webinos travel’ and ‘tripcomputer’
 
Depending on what you show want to show the following URLs are important for you:
·         Desktop-View of webinos travel: localhost:8080/travel-manager/ce/index.html
·         Smartphone-View of webinos travel (screen size of a Galaxy S3): localhost:8080/travel-manager/smartphone.html
·         Automotive View (in-vehicle display): localhost:8080/tripcomputer_review/index.html
This part of the application can be controlled using only key inputs. You can switch between applications, when you press ‘ESC’
 
 
Please let me know, if something is not clear to you.
 
Cheers,
 
Simon