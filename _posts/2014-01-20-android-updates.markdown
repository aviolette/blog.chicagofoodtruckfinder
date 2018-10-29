I’ve made a few improvements to the Chicago Food Truck Finder Android application so that it now includes background sychronization and notifications.

Background synchronizations poll schedule data periodically using Android synchronization framework. Before this change, the application just retrieved schedule data from the server when the application was launched or the user pressed the refresh button. Now, syncs are done on a configurable interval in the background regardless as to whether the application is running.

![Android Settings Dialog](/assets/img/AndroidSettingsDialog.png)

The second feature that I’ve added, is the ability to receive notifications when you are near a food truck. This will popup a notification when you are within ¼ of a mile of a food truck, listing which food trucks you are near. You can enable or disable this notification from the settings dialog. By default, this is off.

Finally, I’ve made some small UI changes to push it in line with website UI (such as displaying “estimated departure” for active trucks).

This will be the last release of the Android app that will support Android versions less than 4.x. In the next release I am going to totally revamp the UI and notifications to support functionality only available in 4.x (and I don’t want to mess around with the compatibility libraries since less than 5% of my users are using this app on the 2.x and 3.x Android versions).