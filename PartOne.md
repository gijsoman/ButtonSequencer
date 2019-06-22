# Part One: Setting Up A Single Button Sequence

## QuickTravel

[Intro](README.md)

[Part Two: Using Multiple Button Sequences](PartTwo.md)

## Result

As promised we will first take a look at the end result.

![](https://gijs-bakker.nl/wp-content/uploads/2019/06/122ca1d9bd7a9c5652390841dfbced9d.gif)

As you can see here there are three buttons that have to be pressed. Each button corresponds to a button on the Xbox Controller. If the correct button is pressed it will disappear and the next button can be pressed.  When all the buttons are pressed a unity event will be invoked to perform an action.

### Features

- Sequence resetting when a wrong button is pressed.
- Sequence timers. A countdown time within which the sequence need to be completed.
- Button Timers. A countdown time within which the button has to be pressed.
- Random Buttons so you don't have to create all the sequences yourself.



## Downloading and Importing the Unity Package

1. Download the Unity Package. As mentioned before this can be done here: https://github.com/gijsoman/ButtonSequencer

2. Open Unity or Unity Hub and create a new project in Unity 2018.3.7f1 or higher (NOTE: older versions probably work but they aren't tested with this package)

   ![UnityCreateProject](/TutorialAssets/UnityCreateProject.gif)

3. Now it's time to drag the downloaded Unity Package into our new project. The following window should pop-up.

   ![Capture](/TutorialAssets/Capture.PNG)

4. Make sure that everything is selected and hit 'Import'. After importing you can see that a folder called "ButtonSequencer" is added to your Assets folder. We are done with importing the Unity Package.

## Setting up the Input Settings

To detect which buttons we are pressing on our controller we need to configure our Input Settings. 

1. Open up the Input Settings window by pressing Edit>Project Settings... In the left panel you see a label called 'Input'. Click on it. You are presented with the following window:

   ![InputWindow](/TutorialAssets/InputWindow.PNG)

2. In the right panel you see the label 'Size' with a number behind it. Change that number to 22 and hit the Enter key. Notice that at the bottom four labels with the word Cancel are added. They are copies of the first input that was already there. These four inputs are for the four face buttons of the Xbox Controller we are going to add.

3. Now we want to add the following buttons: A,X,Y,B. In the example image below I added the A button as an input. Use one of the just created cancel copies for this.

   ![AddedA](/TutorialAssets/AddedA.PNG)

4. For the rest of the buttons you can do the same thing with the rest of the cancel copies. See the results here:

   ![AInput](/TutorialAssets/AInput.PNG) ![BInput](/TutorialAssets/BInput.PNG) ![XInput](/TutorialAssets/XInput.PNG) ![YInput](/TutorialAssets/YInput.PNG)

5. Notice how I used 'joystick button 0' for the A button. This however only works for windows. To see what joystick buttons you need for the rest of your buttons and for your operating system please follow this link: https://wiki.unity3d.com/index.php/Xbox360Controller

6. Now that we are all done with configuring the Input settings let's see how we can set up our first button sequence.

## Setting up the Button Sequence

1. Since all of the prefabs in this package are created with UI elements the first thing we need to do is add a Canvas to our scene. You can do this by clicking the following buttons in the Hierarchy window: Create>UI>Canvas.

   ![CreateCanvas](/TutorialAssets/CreateCanvas.gif)

2. After creating the canvas we can drag in our first prefab. Go to the folder Assets>ButtonSequencer>Prefabs and drag ButtonSequence.prefab into the scene as a child of our just created Cavnas.![FirstPrefabInScene](/TutorialAssets/FirstPrefabInScene.PNG)

   As you can see there is a little square in the middle of our screen. This is the background of our Button Sequence and will resize automatically if we hit play and our Button Sequence is set.

3. Now when we hit play we have a working Button Sequence which is fully functional. You should now be able to press the buttons on your Xbox Controller and you should see the corresponding buttons disappear from the sequence. ![FirstTimePlay](/TutorialAssets/FirstTimePlay.gif)

4. Now that we have a functioning Button Sequence let's check out some of the features we talked about earlier.

## Features and Settings

1. First we want to select the ButtonSequencePrefab in our Hierarchy.

2. After doing this scroll down in your inspector window until you see a component called 'Button Sequence Script'

   ![ButtonSequenceScript](/TutorialAssets/ButtonSequenceScript.PNG)

   Here you can change everything of the Button Sequence.

3. So the first thing we want to check out is the Button Sequence itself. Expand the Button Sequence by clicking the small arrow next to it and let's see what is in there.![ButtonSequenceExpanded](/TutorialAssets/ButtonSequenceExpanded.PNG)

   The first for checkboxes are pretty self explanatory but let's go over each one.

   - Resetting Sequences Allowed: Allows the Button Sequence to be reset when a wrong button is pressed or a timer ended. 
   - Use Random Buttons: One of my personally most used features. With this you don't have to set each button of the sequence yourself. It generates some random buttons for you.
   - Sequence Timer Allowed: Enables a timer within which the sequence has to be completed by the user. You also want to set the 'Sequence Time' for this feature to work properly. If the timer ends the Sequence resets. Resetting Sequences Allowed has to be enabled for this.
   

Then there is a list of the Buttons in our sequence called 'Buttons In Sequence'. We will come back to this later.

At last you see and event called 'On Sequence Completed'. Here you can add your own functions which are called after the sequence is completed. We will also come back to this later.

4. Now let's expand 'Buttons In Sequence' and all of it's elements. You should see the following: ![ButtonsInSequence](/TutorialAssets/ButtonsInSequence.PNG)

   The most important setting here is the Size for the amount of buttons you get in this sequence. If you use Random Buttons you wont have to do much here. However you can set each button manually from the dropdown and you can set a time for each button within which it has to be pressed. Resetting Sequences Allowed is checked automatically.

5. After setting up our sequence we want to do something when the user completed the sequence. For this tutorial we are going to log a message to the console. Please select your main camera in the Hierarchy and add the component called 'LogCompletion' to it.

   ![LogCompletion](/TutorialAssets/LogCompletion.gif)

6. Now we can select our ButtonSequencePrefab in the Hierarchy again and scroll down to the On Sequence Completed event of the Button Sequence Script in the Inspector. Here you want to press the '+' button to add a new entry. Notice a field that says 'None (Object)'. We want to drag our main camera from the hierarchy into this field and select  a function called YouWon(). This function will be fired after completing the Button Sequence. ![AddEvent](/TutorialAssets/AddEvent.gif)

   After doing this a message should be logged to the console after completing the button sequence. Just like the example at the beginning of this tutorial. ![](https://gijs-bakker.nl/wp-content/uploads/2019/06/122ca1d9bd7a9c5652390841dfbced9d.gif)

7. There are still two small features to be explained. The first feature is the Pressed Buttons list. Here you can see which buttons the player has pressed. This comes for debugging if you decide to expand on this tool.

8. The last one is the button Width and Button height. Changing these will make your buttons bigger or smaller.

So next up is using multiple button sequences. Click [here](PartTwo.md) to go to the next part. It will be very short because there are only minor differences.









