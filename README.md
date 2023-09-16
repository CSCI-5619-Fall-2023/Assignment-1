# Assignment 1: Getting Started with VR Development  

**Due: Thursday, September 28, 11:59pm CDT**

The purpose of the assignment is to complete the setup of the virtual reality hardware and software that we will be using in this course and get some experience creating virtual environments in Godot.

## Submission Information

You should fill out this information before submitting your assignment. 

1. **Ready for Grading**. When your assignment is complete, you should change the line below to YES and then push to GitHub. This will signal to the TA that your assignment is ready to be graded. If the submission is completed after the due date, the timestamp of the commit will be used to determine how many late points will be applied.

   `NO`

2. **Third Party Assets**. List the name and source of any third party assets that you added, such as models, images, sounds, or any other content used that was not created by you.

   `TO BE COMPLETED`

3. **Wizard Bonus Functionality**. If you completed the bonus challenge, then please provide a brief description of the additional functionality along with any instructions for the person grading your assignment.

   `TO BE COMPLETED`

## Part 1: Headset Checkout and Setup

**Step 1: Pick up a Headset**

The Quest headsets are available to check out from the [CSE-IT Help Desk](https://cse.umn.edu/cseit/get-help) in Lind Hall L132. You will need to bring your UCard and inform them that you are a student in CSCI 5619. You can keep the headset for the duration of the class, but you **must** return it at the end of the semester.

Note that if you already own a Quest headset (v1 or v2), then you don't need to check out another one from CSE-IT. 

**Step 2: Reset the Headset**

If you turn on the headset and it appears that someone else is logged in, then the previous user most likely forgot to reset the headset after they were done. In that case, I strongly recommend that you complete a [factory reset](https://www.meta.com/help/quest/articles/fix-a-problem/troubleshoot-headsets-and-accessories/troubleshooting-factory-reset-quest/) before continuing further. 

**Step 3: Create a Meta Account**

After you reset the headset, you can follow the interactive instructions to complete the setup. When the Quest was first released, they required using a personal Facebook account, which was very unpopular.  Fortunately, they eventually changed this requirement, and you do **not** need to login using Facebook.

Instead, you will need to create a [Meta account](https://auth.meta.com/) using an email address.

**Step 4: Activate Developer Mode**

In order to build virtual reality applications to the Quest, the headset must be in developer mode. Unfortunately, Meta requires a bunch of extra steps to register as a developer before that option will show up in the headset settings.  If you are running on Windows, you will also need too install the [Oculus ADB drivers](https://developer.oculus.com/documentation/native/android/mobile-device-setup/).

**Step 5: Familiarize Yourself with the Hardware**

If this is your first time using a Meta Quest, it is recommended that you spend some time familiarizing yourself with using the controllers and navigating the menus. There are also several demo games in the Meta store that you can download and try for free, such as Beat Saber and SuperHot VR.

Although the headset itself is rechargeable, each controller requires one AA battery. You are responsible for replacing your own batteries, and I recommend always keeping spares handy in case the batteries die in the middle of working on an assignment!

## Part 2: Getting Started with Godot

**Step 1: Download Godot 4.1.1**

In this class, we will be learning to develop VR applications using [Godot](https://godotengine.org/), a free and open-source game engine.  Note that there are two different versions you can download from the official website. We will be using the standard version in class that uses GDScript, an integrated scripting language with a Python-like syntax. However, you may optionally install the .NET version if you would also like to use C# in your project; however, note that the .NET version won't work for this assignment because the new Godot 4 C# runtime is not yet fully working on Android.

Note that by default, Godot will open scripts in an integrated code editor. This works quite well, and you might find it more convenient when programming using a single monitor. If you prefer to use [Visual Studio Code](https://code.visualstudio.com/) or another IDE, you can set the path to an external editor in Editor->Editor Settings->Text Editor->External.

If you are using VS Code, then I recommend you also install the following useful extensions:

- [godot-tools](https://marketplace.visualstudio.com/items?itemName=geequlim.godot-tools) - Make sure you use "Open Folder" and select your entire project folder for this to work properly!
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - Useful for source control within VS Code.

**Step 2: Getting Started with Godot**

I strongly recommend that you read through the [Getting Started](https://docs.godotengine.org/en/stable/getting_started/introduction/index.html) documentation on the Godot Docs website: 

This will introduce you to the key concepts, design philosophy, and structure of the Godot engine. Although I will be using Godot in the live programming lectures, a complete overview of all the functions in a complex game engine is beyond what we can cover in class. However, as the a widely-used open-source project, Godot has robust documentation and a helpful community. At this point in your CS careers, it is expected that you will be able to consult the documentation and complete tutorials as necessary when learning a new API, toolkit, or game engine.

If you are new to working with game engines, or even if you have experience with other frameworks such as Unity or Unreal, you may find it useful to try implementing the [Your First 3D Game Tutorial](https://docs.godotengine.org/en/stable/getting_started/first_3d_game/index.html).  This is optional and **not** part of the graded assignment.  However, it is a nice introduction a lot of key functionality in Godot, including working with 3D coordinates, using scripting to animate objects, detecting collisions using physics, and more.  Note that although this tutorial was created for Godot 3, it works just fine if you create a new Godot 4 project and then copy over the art assets from their example.

## Part 3: Create a Basic Virtual Environment

To complete this part of the assignment, you will need to create a new Godot 4 project in this folder and then recreate the basic virtual environment that we implemented in [Lecture 3](https://github.com/CSCI-5619-Fall-2023/Lecture-3).  This scene should contain, at minimum, a box representing the ground plane, a simple 3D object such as a sphere placed in front of the user, the XR origin, and the XR camera. You should also place at least one light in the scene so that it's not too dark and 3D objects appear to have some depth.  If you get stuck at any of these steps, then you should go back and rewatch the [video from class](https://mediaspace.umn.edu/media/t/1_gv34dz6q).

We will be working with controller interaction in the next assignment, so you don't need to worry about them for now. However, there is a bonus challenge described in the rubric for adding some controller interaction to this project for those that want extra credit.

At this point, you should set up OpenXR in your project settings and add the initialization script.  This was also covered in class and is described in these [step-by-step instructions](https://docs.godotengine.org/en/stable/tutorials/xr/setting_up_xr.html).

If you have a computer with a VR-capable graphics card, then at this point you should be able to test the project by installing the [Oculus app](https://www.meta.com/quest/setup/) and then running the headset using Oculus Link.

If your computer can't run Oculus Link, then you can also test your application on Windows using the [OpenXR simulator](https://canvas.umn.edu/courses/391288/files/37799241/download?download_frd=1) that has been posted to Canvas. Extract the contents of the zip file into the same folder as Godot, and then click `start_godot_with_simulator.bat`.  This will start the simulator in a separate window and then launch Godot with a temporary environment variable that will hijack the OpenXR runtime. Pretty cool, right? The simulator currently doesn't do that much other than moving the camera side-to-side, but this is sufficient to verify that your project is set up correctly.

## Part 4: Build and Deploy to the Quest

Next, we need to set up the toolchain for building and deploying directly to the Quest. Unfortunately, this requires installing the Android SDK and some additional tools, which is somewhat laborious. On the bright side, though, the Godot documentation provides detailed step-by-step instructions, so make sure you follow these instructions carefully.

**Step 1: Exporting to Android**

First, you will need to follow the general instructions for [exporting from Godot to Android](https://docs.godotengine.org/en/stable/tutorials/export/exporting_for_android.html#doc-exporting-for-android).

**Step 2: Configure OpenXR on Android**

Next, you can follow the instructions to configure your project to deploy to [Android with OpenXR support](https://docs.godotengine.org/en/stable/tutorials/xr/deploying_to_android.html). 

Note that this step involves adding the Godot XR Android OpenXR Loaders to your project assets in the android subfolder. This folder is about 170MB, so I recommend adding  `android/` to the `.gitignore` file so that it won't take up a lot of space in your GitHub repository. However, this means you will need to add the loaders again if you check out the project code on a different computer.

**Step 3: Deploy to the Quest**

After completing all the steps described in this document, you should finally be able to run your project directly on the Quest using the remote debug button at the top-right of the Godot editor for a one-click deploy!

**Step 4: Manually Build the APK File for Grading**

As a final step, you should export your project as an APK file by selecting Project->Export, then select the Android profile you created and click "Export Project." You should save this APK file in the root folder of your git repository. This will allow the TA to verify that your build pipeline is working and will speed up grading. If you want to test the APK file yourself, you can use the [Sidequest](https://sidequestvr.com/) app to manually deploy it to the Quest.

**Getting Help / Helping Others**

There are a lot of steps in setting up this pipeline, so if you run into problems, we strongly encourage everyone to post questions and contribute to answers in the `#assignment-1` channel on Slack. Additionally, although these tools have cross-platform compatibility, there is also the possibility encounter unforeseen issues on different operating systems. Asking other students or providing assistance with the installation and configuration of the Android build pipeline described in this part of the assignment is completely fine and will **not** be considered a violation of academic honesty.

## Part 5: Customize Your Scene

To complete this assignment, you should extend your scene a bit beyond what we did in class.  The minimum requirements are:

1. Add at least four more 3D objects to the scene. These can either be graphics primitives (boxes, spheres, cylinders, etc.) or 3D models you find online.  If you use third party assets, make sure that all models are low poly so they don't slow down your Quest. Note that all third party assets **must** be properly documented at the top of this readme file!
2. Move each 3D object to different location around the user. 
3. Add a script that animates at least one of the 3D objects. You can make the object do anything you want, as long as the object uses the `_process()` function to continuously move in every frame. You can change the object's translation, rotation, scale, or any combination of the three.

## Rubric

Graded out of 20 points.

1. Created a project with the basic geometry described in Part 3. (2)
2. XR origin and XR camera are set up correctly in the scene. (2) 
3. Submission includes APK file generated by running the Android build described in Part 4. (4)
4. Running the APK on the Quest successfully initializes OpenXR with a head-tracked camera. (4)
5. At least four more 3D objects added to the scene in Part 5. (2)
6. New objects are placed in different locations around the user. (2)
7. At least one of the objects in the scene is animated using a script. (4)

**Bonus Challenge:** For two points of extra credit, you can look ahead a bit at the documentation on [XR controller input](https://docs.godotengine.org/en/stable/tutorials/xr/xr_action_map.html) and add some interaction with the 3D objects using the hand-tracked controllers. This is an open-ended challenge, and creativity is encouraged! Make sure to describe any additional functionality at the top of this readme file so that we can properly test it during grading. (+2)

**Documentation:** Make sure to document any third party assets or code used in this assignment at the top of this readme file. One point will be deducted for using third party assets without attribution. This only refers to additional assets that you find on your own; you don't need to document anything that is already described in the assignment instructions. (-1)

## License

Material for [CSCI 5619 Fall 2023](https://canvas.umn.edu/courses/391288/assignments/syllabus) by [Evan Suma Rosenberg](https://illusioneering.umn.edu/) is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).
