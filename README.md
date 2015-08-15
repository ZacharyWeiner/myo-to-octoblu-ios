# myo-to-octoblu-ios

This application transforms the Myo Armband into a remote control for any Octoblu.com flow. 

Each Gesture that is recognized by the Myo is liststed in the codes application controller, in a single switch statement. 

The statement determines what data to put into the POST request, but if you just want to use the webhook as a trigger, you may not need to apss custom data. 

This demo is attached to an OctobluFlow <insert_blueprint_link> that changes the color of a Blink LED light, but you can package up any data you like into the POST request to be recieved by the flow. 

In order to make the light change color you must:

	Set Up Octoblu:
		1. Create an Account on Octoblu.com 
		2. Import the blueprint <insert_blueprint_link>
		3. Download Gateblu

	Then you can replace the webhook address in the iOS Apps - application controller, with the webhook from the trigger in the flow that resulted from importing the blueprint 

	To Use the Application 
	1. Launch This application on your iPhone or iPad 
	2. Pair your Myo Armband to the Device 
	3. Make Gestures 
		3.a Perfrom Sync Gesture 
		3.b Make Fist twice to mimic a "Double Click" to unlock the app
	4. Verify that your Octoblu flow is running, and that data is coming into the request (using the debug output)
	5. Attach a Blink (or repalce the blink node with any other node)
	6. See Blink Change Color when you make new Gestures. 

Note: The Myo is very sensitive and must be calibrated for every user. The iOS Application will display the name of the gesture it is currently recognizing so that you can know what data it should be sending up to Octoblu.com 