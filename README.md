# GBL-Performance-Task

# OVERVIEW

For this task, you will implement a simple tool/game that tests a few basic Unity skills. The program will essentially allow users to create objects, delete objects, and make objects spin. Created objects will be placed in a grid of a variable size that can also be set by the user. An example layout for the tool can be seen below.

Some of the project has been given to you already, with instructions on how to duplicate the repository to your own Github account later in this document. Be sure to log your changes in Git as you go (as you would with any project).
 
![Example](Example/ExampleLayout.png)
 
In this example, the dimensions of the grid are set to be 4x4, there have been 14 objects created, and the 5th object (1st object in the second row) is set to be spinning.

The required features are as follows:

- The user can add objects by click of a button. These will be placed in the next available grid slot (if available).
- The user can remove objects by click of a button. The last object (bottom-rightmost) will be deleted from the scene (if available).
- The user can change the dimensions of the grid by use of an input field. The dimension change can be triggered by a change in the input field or by a confirm button press.
- The user can click a cube to make it spin (and click it again to make it stop).


# FEATURE OBJECTIVES

The requirements of different mechanics of the tool are described in more detail below.

## UI INTERACTION

Interaction between UI elements such as buttons or input fields must trigger the execution of code in order to fulfil the requirements stated above.

## OBJECT SPAWNING/DESTROYING

Objects should be instantiated and destroyed using standard Unity functions. Objects created must be created using a prefab as a template. This means you must first create a prefab with whatever components necessary to complete the task. In my example above, I created a Cube and attached an Animator component, which I then assigned an Animator Controller to (you will be provided with an Animator controller under Assets/Art/Animators).

## OBJECT PLACEMENT

Objects’ position must be calculated so that they are displayed in a grid formation. This calculation should account for varying dimension sizes set by the user.

## ANIMATOR CONTROLLER INTERACTION

When an object exists in the world, it can be clicked to make it spin. This is done by setting an Animator Parameter within the Animator component of an object. You will not have to create the Animator Controller or Animation, these are provided in the project. You will, however, have to add an Animator component to your cube’s prefab (or whatever object you use) and assign the given Animator Controller to this component.

## EDGE CASE HANDLING

You will need to handle edge cases as you see fit. As an example, will the “Add” button still be clickable when the grid has been filled up?


# PERFORMANCE OBJECTIVES

Outlined below are other metrics by which you will be evaluated.

## SOURCE CONTROL ETIQUETTE

You should make small, frequent and commented commits to your duplicate repository.

## PROJECT ORGANIZATION

Scripts, prefabs, and all other files and objects should be well maintained in a clear and clean file structure.

## CODE READABILITY

Code should be consistent and understandable.

## CODE QUALITY

Good practices should be implemented when maintaining collections of objects, writing functions or loops, or developing in general.

## DOCUMENTATION

Code should be reasonably commented, whether they are header comments for classes or functions or just in-line comments describing a complex operation. These comments should be understandable and frequent, but not excessive (you don’t need to comment every single line).


# WHERE TO START

To begin this performance evaluation, you will need Unity and a Github account. It is also recommended that you use Visual Studio as your editor, which can be included from the Unity Installation. Even though you may have used these tools before, follow the simple steps below to ensure you are set up for the task properly.

## INSTALL UNITY

We will use Unity 2018.4.1f1 (Personal) for this performance task. Other versions may work, but the project is set up with this version, so it is recommended that you use it. If you have another version of Unity installed and do not wish to replace it, you can simply specify a new install location beside the old one (Unity typically installs to `C:/Program Files/Unity` but I often change this to something like `C:/Program Files/Unity 2018` so that I can switch between versions if needed).

This version of Unity (2018.4.1f1 Personal) can be found at https://unity3d.com/unity/qa/lts-releases. Choosing the Unity Editor Download Assistant should give you everything you need (the default settings should install Visual Studio 2017 and properly port it to the Unity install).

## DUPLICATE GITHUB PROJECT
If you do not have a Github account already, you will need to create one. After account creation, you can set up a copy of the initial repository and begin working.

NOTE: DO NOT fork the below repository, forked repositories cannot be made private. To maintain privacy of all candidates for the position, you should duplicate the following repository so that you may mark it private on Github. To accomplish this, follow the instructions below.

1. Sign into Github (create an account if necessary)
2. Click to create a new repository (Repositories Tab > New)
3. Click the link to Import a repository
4. For the old repo’s clone URL, add https://github.com/bradenroper/GBL-Performance-Task.git
5. Mark the repository as Private
6. Give the repository a name (I’m not picky)
7. Click to Begin Import 
8. Wait a minute or two while Github creates the duplicate repo
9. Navigate to the new, private repository (User Icon in top right > Your Repositories)
10. Open the Settings tab and select Collaborators on the left menu
11. Add me (bradenroper) as a collaborator so that I can see your work
You can now begin working but remember to commit and push your work as you go!

 
# HELPFUL HINTS

Some helpful areas of Unity documentation for this project are listed below.

- Prefabs: prefabs are useful for many reasons, including being used as a blueprint for spawned objects
https://docs.unity3d.com/Manual/Prefabs.html
- Animator Parameters: setting these ultimately changes what animation state will be transitioned to.
https://docs.unity3d.com/Manual/AnimationParameters.html
- Raycasting: this is used to determine if clicks hit in-world objects, like detecting clicks on a cube.
https://docs.unity3d.com/ScriptReference/Physics.Raycast.html
