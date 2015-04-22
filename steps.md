

Make a New Project, Single View Application:

![](images/screenshots/image02.png)

![](images/screenshots/image03.png)


# Create the Tab Bar Controller

Delete the View Controller

Find the Tab Bar Controller in the lower-right list of UI Elements, then drag it onto the canvas

![](images/screenshots/image04.png)

![](images/screenshots/image05.png)

Tip: We can ctrl-click canvas to bring up the zoom menu and zoom out or in.  
![](images/screenshots/image07.png)

Select the Tab Bar Controller, and in the right panel in the properties section,
- In Simulated Metrics, choose a size to match your devices
- Check 'is Initial View Controller'

![](images/screenshots/image08.png)

Run

## Name the tabs
Select the tab bar item (either in the left list view or on the layout view)
![](images/screenshots/image09.png)

then in the properties panel (on the right), type the name in Bar Item section, Title field

![](images/screenshots/image10.png)

## Add images
In the file list on the left side, select Image.xcassets, then we can drag in the images of our screens from our Finder window into Xcode.

![](images/screenshots/image11.png)

Then back in the storyboard, find an ImageView

![](images/screenshots/image12.png)

and drag onto on of the tab ViewControllers, and choose an image for it

![](images/screenshots/image13.png)

and again for the second tab:

![](images/screenshots/image16.png)


Now here's what I've got for my first two tabs:

![](images/screenshots/image14.png)  ![](images/screenshots/image15.png)

## Add a third tab

Ctrl-Click and drag from the Tab bar Controller to our new ViewController, a popup menu will appear:

![](images/screenshots/image17.png)

Choose "View Controllers" under "Relationship Segue"
and a new arrow will appear

![](images/screenshots/image18.png)

Drag in an image view and name the tab, add the image for the third tab

Run -- tabs work but things are sized incorrectly

![](images/screenshots/simulator0/anim.gif)

## Sizing the Screens
Size classes are a new feature of iOS 8 and Xcode 6, allowing you to have one storyboard for universal apps.

Select an ImageView for one of the tabs, Under menu Editor > Pin >
- Top Space to Superview
- Leading Space to Superview
- Trailing Space to Superview
- Bottom Space to Superview

Do this for each image

## Adding Tab Icons

The images for tab bars and toolbars are actually alpha masks, not complete images. Only the alpha channel of the image is used.

With preview, we can use the magic want to create an image with an alpha channel

![](images/screenshots/image22.png)

![](images/screenshots/image23.png)

![](images/screenshots/image24.png)

![](images/screenshots/image25.png)

![](images/screenshots/image26.png)

![](images/screenshots/image27.png)

Drag the icons into xcassets
![](images/screenshots/image28.png)

Set the image of each tab

![](images/screenshots/image29.png)

We should see it change like this:

![](images/screenshots/image30.png)

Now our prototype app has three tabs:
![](images/screenshots/image01.png)

![](images/app2.gif)
