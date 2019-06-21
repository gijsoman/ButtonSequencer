# Part One: Setting Up A Single Button Sequence

As promised we will first take a look at the end result.

## Result

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

2. In the right panel you see the label 'Size' with a number behind it. Change that number to 22 and hit the Enter key. Notice that at the bottom four labels with the word Cancel are added. They are copies of the first input that was already there. These four inputs are for the four face buttons of the Xbox Controller. 