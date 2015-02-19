# prototyping-curriculum
An in-progress ios-app-prototyping curriculum intended for railsbridge-like workshops. 

Obviously this is not usable yet. Submit a pull request or issue if you'd like to help. 

# Goals
- Get students talking
- Show students that they know stuff about iOS
- Introduce Some standard iOS building blocks
- Super quick preview of interface builder
- Hand-Wavy Language for talking about iOS code e.g. ViewController

# Open questions

- When does this exercise happen? after tip calculator? before? beginner? intermediate?
	- maybe this happens at the end as a wrap up/review? 
- What is the "product" built? Is it deterministic? or is there a brain storming session? 
- Could the teachers "pair" on this exercise? Two keyboards, one types the other navigates? 

# Teacher Background Knowledge
- 3 most common types of navigation
	- tabs (tab bar with buttons at bottom of screen)
	- push (navigation controller)
	- modal (rise from below)
	- custom (e.g. hamburger menu)
	
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