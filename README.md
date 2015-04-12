# prototyping-curriculum
An in-progress ios-app-prototyping-for-designers curriculum intended for railsbridge-like workshops.

This is not usable yet. Submit a pull request or issue if you'd like to help. 

# Goals
- Get students talking
- Show students that they know stuff about iOS
- Introduce Some standard iOS building blocks
- Super quick preview of interface builder
- Hand-Wavy Language for talking about iOS code e.g. ViewController

# Target Audience
- Designers little or no programming experience
- or expert programmers new to xCode

# Before this
TipCalculator: simple app to teach basic concepts. Goal to get a feel and familiarity with XCode and to see the languague (but not learn everything)
-
-


# Open questions

- What is the "product" built? Is it deterministic? or is there a brain storming session? 
	- d 	
- Could the teachers "pair" on this exercise? Two keyboards, one types the other navigates? 
- Suggest friday night session on app ideas
- disable auto layout? 

# Teacher Background Knowledge
- 3 most common types of navigation
	- tabs (tab bar with buttons at bottom of screen)
	- push (navigation controller)
	- modal (rise from below)
	- custom (e.g. hamburger menu)

# Part 1 - Brainstorm an app
- Show them UI patterns 
	- pttrns.com
	- mobile-patterns.com
- Collect ideas for apps (go around the room and have students share an idea for an app)
	- for eachish idea, interject with an idea of a pattern that might apply (point to one in pttrns.com maybe)
- hand out iPhone sized paper for drawing prototypes with instructions to actually write real sample text (not squiggles)
- give students 15-20 minutes
- have them "usability test" on other students 
	- Suggest the kinds of questions to use as prompts in a usability test
		- what do you think when you've gone to this screen
		- you've just signed up with facebook what do you think this app does 
		- you're trying to find a restaurant. What would you click on this screen
	- test subjects should speak aloud what they think 
		- I think I should type my name here. 
		- I think this arrow will show me the address of the restaurant
- 10 minutes to revise screens based on feedback. 
- take iPhone photos of prototype screens
- in preview cut out the pieces and add them to xcassets (may require tools->adjust size since iphone photos have all the pixels)
- use them as backgrounds for image views
- create navigation controllers natively (an ideal app for this exercise uses standard navigation: 1. tabs 2. push reveal 3. modal)
- you should have a working wireframed app with hardcoded example data from paper mockup. 
- Hurray!



#5 things that are special about phones
- Geolocation
- personal (contacts...)
- accelerometer
- camera / microphone / flashlight / photo / video / audio recording
- gestures


	
# Questions/Actions that drive the class

- What are some ways of getting from one screen to another in an iOS app (students should have some intuitions here. egg them along and write down what they say)
- ... ? 
- Drag assets into xcassets
- Who remembers how to disable auto layout? ()
- drag an image view into the first view controller
- Set a specific image in the UIImage View
	- How do I change properties of views? (get the students to remember this and tell you how to do it)
- I'm going to wrap a navigation controller around this view controller (Editor > Embed In > Navigation Controller) Now I have this navigation bar
- How do I know when to go to the next screen... right, let's add a button. 
- Now that button needs to trigger a transition to another screen. We need a new ViewController to control the new screen. 
- Now create the code to go with the ViewController in the storyboard. iOS panel ->  Source > CocoaTouchClass
	- Name it correctly, case matters: UpdateStatusViewController. 
	- It needs to be a subclass of UIViewController
- drag in a view controller, you'll need to select the little yello bal to be able to find it in the list
- Now go to the drivers license. The drivers licence tells you who you are. Here we write the name of the view controller so xcode can link up the viewcontroller in the nib with the code for what it does. 
- drag in a cancel button. 
- we're going to add behavior to the button. right click it and drag it and drop it in the viewcontroller's implementation. 
- select action (and not outlet)
- in the code for the outlet, we want to make the view controller dismiss itself. 
	- 	[self dismissViewControllerAnimated:YES completion:nil];


#Review Questions

- What information is in a nib? why are nibs separate from the code that describes their behavior?
- what is a view controller? 
- what are three ways of navigating from one screen to another? 
- 