# Project 1 - *Name of App Here*

SimpleTodo is an android app that allows building a todo list and basic todo items management functionality including adding new items, editing and deleting an existing item.

Submitted by: Esteban Luques

Time spent: 6 hours spent in total

## User Stories

The following **required** functionality is completed:

* [x] User can **view a list of todo items**
* [x] User can **successfully add and remove items** from the todo list
* [x] User's **list of items persisted** upon modification and and retrieved properly on app restart

The following **optional** features are implemented:

* [ ] User can **tap a todo item in the list and bring up an edit screen for the todo item** and then have any changes to the text reflected in the todo list

The following **additional** features are implemented:

* [ ] List anything else that you can get done to improve the app functionality!

## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src='https://github.com/HIPERION2021/Simpletodo-2/blob/master/simpletodo2.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Android Studio installed sucessfully but the AVD failed to initialize. 3 different issues needed to be adderssed.
1.- x86 Intel acceleration showed as istalled (as per SDK tools) but the service was not running, x86 acceleration needed to be reinstalled to solve the issue.
2.- AVD failed to load due to missinf amdvlk64.dll and amdvlk86.dll. The dll files were downloaded and registered but the issue persisted. To overcome the 
error VULKAN was disabled by creating a file called advancedFeatures.ini inside the .android folder with the following options:

Vulkan=off
GLDirectMem =on

3.- In addition, the acceleration method needed to be changed, but Android Studio disabled the option and set the parameter to "Automatic". To change this parameter
manually the config.ini file needed to be edited.

the line hw.gpu.enabled was setted to "no" (by default is "yes")  

The above descibed steps solved the issue and AVD started normally.

## License

    Copyright 2021 Esteban Luques

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
