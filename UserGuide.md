##What is Match on the Street?
Match on the Street allows users to create, find, and join sports events spontaneously. It targets both casual and avid sports players who want to be able to connect with other players near them, in real time. Currently, sports meetups are formed based on either the luck of the draw for a simple pick-up game or having already formed a group meetup plan. With Match on the Street, you can find people whenever and wherever you want. In other words, you get all the benefits of long term planning, but none of the guesswork of regular pick up sports. 

#Basic functionalities

##If you are using this application for the first time:
1. Go to the ".apk file" download link in the Downloads section of the page, preferably on the Android device you want to install this application to (if not, the .apk file has to be transferred to the local storage of the device).
2. Open the .apk file on the Android device and allow the application access permissions, the system package manager should initiate the installation process automatically.
3. Once the installation is complete, the application icon should appear in the home screen or app drawer of the device.

##Browsing Events
MOTS has two primary ways to browse sporting events that work similarly to Yelp: 
* The Map, where you can visualize the events happening around you or a specific area.
  1. Works just like google maps where you can find your location and see the events around you.
  2. The search bar can be used to see events in a specific location. Eg. searching “Seattle” will display the events around Seattle.
* The List, which allows you to search and filter down events to your liking. 
  1. To apply a filter on search results (e.g. names with “basketball”), swipe down when at the top of the list, and type “basketball” into the search bar.
  2. Selecting an event from the list will bring up another screen with the details of that event. Pressing the back button from here will return you to your search results.
  3. Clicking on the back button or the floating action button with the map icon will bring you back to the map view.

##Creating Events
If you can’t find a sporting event that fits your requirements, you can create your own! Events can be created from the Map View by tapping and holding on the desired location. On the create event screen you are able to detail the sporting event in several ways:
* A title (the first thing other people will see, should include name of sport)
* The time and approximate duration of the event 
* A description (any special notes or requirements e.g. need to bring cleats or a ball. Or notes on where to meet.)

##Viewing your Events
Opening your profile will allow you to see the events you are attending. To do this swipe from the left-hand side of the screen to bring up the sidebar and tap the “My Events” item. This will bring up a screen that has all the events you are attending and tapping on an event will allow you to view the specific details and unattend the event if desired.

##Logging in and out
The option of logging in/out could be found in the "Facebook Login" item in the sidebar.
When you are using the app for the first time, you will be automatically prompted to this page to log in with a Facebook account. After you have logged in, the "Log in with Facebook" button will be replaced by "Log out". By tapping on the "Log out" button you wiil log out of the application.

#Components of the Application
##Map View
The map view is the main component of the application. You can use it to browse around and find events by their locations.

![map-view](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-map.png)

The search bar is used to find a certain location. If the name or address of a location is entered and the search icon is tapped, the map will be zoomed to this specific location, if it exists.

The three buttons, from top to bottom, are:
* *Zoom to user location*: When tapped, the camera is moved and zoomed in to the user's location, if it is available.
* *Switch to List View*: When tapped, the currently displayed events are transfered to a list format in the List View, in which you can further filter and search for specific events.
* *Refresh events*: When tapped, the information of the events are refreshed within the current screen selection. When the map is panned around, it is recommended to use this button to acquire new events.

The different markers denote the location of different events. When the marker is tapped, its details will be shown as below:

![detail](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-detail.png)

The detail section displays the title, description, date, duration and participants for the events. The toggle button in the lower-right corner will allow you to join or leave a certain event.

##List View
The List View could be access from the Map View by tapping on the "List" button. It is used to intuitively display title/descriptions of events, and to filter/search for specific events.

![list-view](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-list.png)

By tapping on any of the events, you will be transfered to the Map View displaying the location and the detail section of this event.

By continuing scrolling/swiping down when at the top of the list, you will bring up the options for searching/filtering.

![filter](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-filter.png)

The fields for top to bottom are respectively:
* *Keyword Searchbar*: You can type any keywords that you wish the resulting events to contain.
* *"From" date*: Double-tap on this entry will bring up a date picker. You can pick the date after with the resulting events start.
* *"To" date*: Similar to "From" date, except that it specifies the date by which the resulting events end.
* *Search radius*: Typing a number in the entry will narrow the results into events that are within this radius.
* *Apply button*: By tapping on this button, all the filled-in entries will be collected and used in the filter. The list of events will refresh according to the specified filter.

![filter](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-filter-after.png)

After applying the filter, you can tap on the "Map" button at the lower-right corner of the List View to inspect the filter results on the Map.

##Sidebar

![side-bar](https://github.com/MatchOnTheStreet/Docs/blob/master/img/ss-sidebar.png)

The sidebar could be accessed by swiping from the left on screens on which you can see the hamburger button (Normally, the Map View). It contains: 
* *Map*: A shortcut to the Map View.
* *My Events*: The view in which you can inspect all the events you are attending.
* *Facebook Login*: The view in which you can log in/out of the application using a Faceboook account.
* *Report a Bug*: The link to the webpage where you can report a bug.
(In current release the "Settings" item does not have any functionality.)



