# Control LED with Google Assistant  
### Using Google Assistant voice commands to control an LED  
<br/>

***Overview :***  
This project uses [Blynk IoT platform](https://blynk.io/) and [IFTTT](https://ifttt.com/) Applet to control an LED connected to a NodeMCU via the voice commands. Other voice assistants like Amazon Alexa and Siri can also be used, but the process to integrate Siri with IFTTT is a bit different to that of Alexa and Google Assistant.  
<br/>  

***Required Components :***  
- Mobile Phone - iOS or Android
- NodeMCU - ESP8266
- Resistor - 1K Ohm
- LED - Any colour
- Breadboard and Jumper Wires (Male to Female)  
<br/>

***Software Requirements :***
- Arduino IDE
- Blynk Web and Mobile applications
- IFTTT Account  
<br/>

***Blynk IoT Platform Tutorial :***  
Watching a video is much funt than reading through an article. Hence, go through [this playlist](https://www.youtube.com/playlist?list=PLruzZCuhcsGNrSxeWer6C0vff7hq37Num) by [Techiesms](https://www.youtube.com/channel/UC7raRsx4ojx3cyXT3x9-PuQ) to understand and learn the basics of Blynk IoT Platform and create your first LED blinking project. It is better if you go though the playlist, especially the [First Project](https://www.youtube.com/watch?v=IKbbvEzZ7wg&list=PLruzZCuhcsGNrSxeWer6C0vff7hq37Num&index=2) and [APIs](https://www.youtube.com/watch?v=uPMibJhrtjE&list=PLruzZCuhcsGNrSxeWer6C0vff7hq37Num&index=5) videos in order to understand the next part on integration of Google Assistant and IFTTT.  

After creating your first LED blinking project, it's now time to move on a step further and integrate it with Google Assistant.  
<br/>

***IFTTT Integration :***  
Go to [IFTTT website](https://ifttt.com/). Create an account and login if you are not already a user. Then proceed to creating a new Applet, by clicking on `Create` button on the top right corner. Follow the steps below to setup IFTTT with Google Assistant.  
- Click on the `If This` section and type `Google Assistant` into the search bar. It will then ask you to integrate the Google Assistant Service by logging in to your Google Account. Make sure you login with the account that you use in your mobile phone.
- Next select `Say a simple phrase` option.
- Type in the voice command that you would like to use, and any other ways to say it. Then click on `Create Trigger`.
- Now click on to the `Then That` option and search for `Webhook` service.
- Once the Webhook Service is activated, you will be asked to fill in a URL. Type in the URL of the API for your Blynk Device. To find out your own API link, watch [this video](https://www.youtube.com/watch?v=uPMibJhrtjE&list=PLruzZCuhcsGNrSxeWer6C0vff7hq37Num&index=5)
- Select `Get` method and leave the rest as they are.
- Select `Create Action`. 
- Finally, save your Applet.  

You'll need to create 2 applets, one for turning on and the other for turning off the LED. Give a few minutes for the Applet to configure and then open your mobile phone. Try saying the phrase to the Assistant and voila, your LED is now being controlled by voice commands. Similar steps can be followed for Amazon Alexa too. just replace the Google Assistant search with Alexa and then proceed with the next steps.  
<br/>

***Setting up Voice Control using Siri :***  
Setting up Siri in IFTTT is not direct as Siri is not available as a direct service. Hence, we use the `iOS Shortcuts` app in addition to IFTTT. Download the IFTTT iOS application from the App Store and then follow the below steps to create a new Shortcut.  
- Create an IFTTT Applet just as for Google Assistant, but for the trigger, select `Button Widget` instead of Google Assistant. 
- Use the same Blynk API URL and other settings and create an applet.
- No head over to the shortcuts app and create a new shortcut. 
- Now add a new action, and select IFTTT app. 
- Select, `Trigger Applet` option from the selection menu.
- Now choose the previously created applet from the selection menu. 
- Name the shortcut with an appropriate phrase. This phrase is used to execute voice command in Siri.
- Now save the Shortcut.  

Voice Commands run in Siri take more time to run than in the Google Assistant, as Siri needs to process the command through Shortcuts app too in addition to IFTTT.  
<br/>

### More info will be added soon!!