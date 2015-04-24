
UITableView can display and edit a list of data. It can be displayed vertically but not horizontally. Each item in the table is displayed as a UITableViewCell.

This tutorial goes through the steps for creating a simple list as its own project, but you can also use these steps to add a tableview and details screen into another app within a tab bar or after a log in screen.  (Screenshots are from Xcode 6.2 / Yosemite, but should be similar to later 6.x versions of Xcode.  Note that early versions of Xcode 6 had bugs )

Create a new project.  Choose "Single View Application."

![](images/tableview/image00.png)

![](images/tableview/image01.png)

The initial project screen will look like this:
![](images/tableview/image02.png)

The project starts with a ViewController, but we want to use a different kind of controller, so click on Main.storyboard, select the View Controller and delete:
![](images/tableview/image03.png)

Then select a Navigation Controller (in the lower-right)...
![](images/tableview/image04.png)

and drag onto the canvas, then select iPhone size for the simulated metrics:

![](images/tableview/image05.png)

which makes it easier to work with in storyboard view:
![](images/tableview/image06.png)

Run

![](images/tableview/image07.png)

Need to set the Navigation Controller as the Initial View Controller.

![](images/tableview/image08.png)

Now, when you run the app, you should see:
![](images/tableview/image09.png)

Give your table view a title:
![](images/tableview/image10.png)

Now we need to create the companion code files to go with the tableview, and another for the view to add an item to the list.

![](images/tableview/image12.png)

![](images/tableview/image13.png)

![](images/tableview/image14.png)

![](images/tableview/image15.png)

![](images/tableview/image16.png)

![](images/tableview/image17.png)

![](images/tableview/image18.png)

Now we'll make a custom UIViewController for the screen to create a new list item:

![](images/tableview/image19.png)

![](images/tableview/image20.png)

Drag out a ViewController and specify the custom class:

![](images/tableview/image21.png)

## Create the Add Button [+]

![](images/tableview/image24.png)

![](images/tableview/image25.png)

![](images/tableview/image26.png)

## Connect the Add button to the new item view

![](images/tableview/image27.png)
![](images/tableview/image28.png)
![](images/tableview/image29.png)


![](images/tableview/image30.png)

## Add cancel and save buttons to the new item view

![](images/tableview/image31.png)
![](images/tableview/image32.png)
![](images/tableview/image33.png)
![](images/tableview/image34.png)
![](images/tableview/image35.png)
![](images/tableview/image36.png)
![](images/tableview/image37.png)


## Change View When Cancel / Save 

In the ListTableViewController, add
```
@IBAction func unwindToNoteTableViewController(segue: UIStoryboardSegue) {
}
```
before the last } at the end of the file.

Ctrl-drag from "Cancel" to the Exit icon and choose "unwindToNoteTableViewController" from the menu.
You can do the same with "Save" which works for a mock up -- later you would need to write code to actually save the data.

## Create new item view elements

Ctrl-click on the Text Field and drag to the left edge of the View.  Then select from the popup menu:
- Leading Space to Controller Margin

Do the same with the right edge, selecting "Trailing Space to Controller Margin"


Do the same with the top edge, selecting "Top Space to Layout Guide"

Run, rotate the phone simulator (command-arrow) and see the text field resize.

Add a label, ctrl-drag up, select "Top Space to Layout Guide"
now ctrl-drag up again, choose "Center Horizontally in Container"
