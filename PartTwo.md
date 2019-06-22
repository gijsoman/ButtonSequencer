# Part Two: Using Multiple Button Sequences

First let's look at the end result again.

## Result

![MultipleSequences](/TutorialAssets/MultipleSequences.gif)

So there's not much difference from using multiple Button sequences than just using one. The only thing we have to do is change our prefab.  There is a little bit more functionality I want to go over later in this tutorial though. First let's start with setting up multiple Button Sequences.

## Setting up Multiple Button Sequences

1. Delete or disable the ButtonSequencePrefab in the Hierarchy.

2. Now from the folder Assets/Prefabs let's drag MultipleSequenceManager into the hierarchy as a child of Canvas just like we did with our ButtonSequencePrefab.

3. Select it in the Hierarchy and look in the Inspector for the component called 'Multiple Sequences Manager'.![MultipleSequencesComponent](/TutorialAssets/MultipleSequencesComponent.PNG)

   As you can see there is an 'On All Sequences Completed' event which works the same as the 'On Sequence Completed' event of a single Button Sequence. I already put the YouWon() function in here to save you some time. 

4. So besides the event you see a couple of things. A button Sequence Prefab which is just a reference to the prefab of a single button sequence. We can leave this be. Below that there is a field for a 'Sequence Object'. This is the extra functionality I was talking about. We will talk about this later. For now you can just expand 'Button Sequences' By clicking the little arrow next to it. Also expand the elements inside of it.

5. You are presented with the following:

   ![ExpandedMultipleSequences](/TutorialAssets/ExpandedMultipleSequences.PNG)

If you have followed the first part of this tutorial this should look pretty familiar. If you haven't and this looks unfamiliar to you please follow the first part of this tutorial. I won't go over the settings of a single sequence again since they work exactly the same. The only thing that is different is that you can set the amount of Button sequences you want by changing the number behind 'Size'. I would highly recommend just experimenting with the settings and if you need anything specific you can take a look at the first part of the tutorial again. There is one thing we didn't have in the first part though. Let's take a look at this.

## Using a Scriptable Object 

So previously I wrote about the 'Sequence Object' field which is currently empty. In this field we can put an object of the type 'SequenceObject' which can be created in the project window. We can use this Sequence Object to create multiple Button Sequences in a separate file. This comes in handy when you are making long lists of sequences and your inspector is becoming to flooded with information. It is also very nice for making different types of Sequences. This way you don't have to change every setting for each object that has multiple button sequences. Instead you can just drag in the Sequence Object you want that object to use. 

1. Navigate to the folder Assets/SequenceObjects. Here you see a file named SequenceObject. You can ignore this file for now because we want to make our own. Right click somewhere in this folder and select Create>SequenceObject.![SequenceObjectCreation](/TutorialAssets/SequenceObjectCreation.gif)
2. Now select the sequence object and notice that in the Inspector you can change all the settings for multiple button sequences.

![SequenceObjectCreation2](/TutorialAssets/SequenceObjectCreation2.gif)

3. Now the only thing we have to do is drag this object into our Multiple Sequence Manager and it will override any settings made here. Our Multiple Sequence Manager is now using our Sequence Object.![DragginSequenceObject](/TutorialAssets/DragginSequenceObject.gif)

   If you see the following after hitting play you forgot to set the amount of buttons for each sequence in your Sequence Object:![ForgotButtons](/TutorialAssets/ForgotButtons.PNG)

   Thanks for using my tool and following this tutorial. Feel free to expand on this tool and use this code in any way you like. I hope it makes your life a little bit easier.

   

   





