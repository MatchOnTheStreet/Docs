User Test Guidelines

# General Process

The usability study should cover most of the application’s functionalities, including: 

* Logging into the app

* Browsing/attending events on the map

* Searching for events in the list

* Viewing the events that are marked as attending

* Logging out of the app

We decided to give the user freedom to explore so that we can gain useful insights on our application. The user are allowed to know the general purpose of the application ("Browsing, creating and attending sporting events"). However, concrete instructions on certain procedures should be avoided unless the user has become completely clueless. 

The overall process of the tests should resemble the following:

1. The user is informed that he/she will be involved in a usability test of a mobile application called *MatchontheStreet*, which is used for organizing/attending sporting events.

2. Choose from:

    1. The user has an Android device and is guided to the product website where he/she can try to download/install the application.

    2. The user is given a device with the application freshly installed.

1. The user is given time to explore the application on his/her own. Meanwhile, the developer should record:

    3. Tasks among the list that the user was able to perform smoothly without further hints.

    4. Tasks among the list that the user had difficulties/failed to perform and a description of the situation.

    5. Any opinions or suggestions from the user in the process (both functionally and aesthetically).

2. The test conductor wraps up the test by asking the user for advices on improving the application.

User Test Results

# Case One

**User:**

* Biology major

* iOS and Apple user

* Told the description of the app and nothing else

 

**Good:**

* Familiar with google maps and understood the current location button, and the refresh button

* Understood that tapping on the icons would bring up the details of the event

* Easily understood how to attend/unattend an event

* Easily reported a bug

**Bad:**

* Not clear what the icons represent, made worse since the icons change every time the events are refreshed

* Entering all the fields in the list view didn’t return any results even though there should have been

* Thought that pressing the map button on the list view would take him back to the original maps screen and wondered where the icon went

* Not clear on what the From or To dates are for since it doesn’t make sense to search for events in the past.

* Not clear how to create an event

* Wasn’t aware of the sidebar

* Wasn’t aware of the search button in the maps view

* Wasn’t aware of how to search or filter results on the listview (scrolling all the way up)

* Emphasis on wanting to be able to edit or delete an event

* When selecting an event on the MyEvents user expected it to show the event on the map

* Wondering why there’s a logout button on the MyEvents when there’s already a facebook screen to logout

* Hidden google maps button under the attend/unattend button would redirect to the google maps app 

**Improvements:**

* Icons are clear and no longer randomly chosen

* Bugs with the filtering have been resolved

* Transitions between the map and the list view are better aligned with what the user would expect.

* Removed the google maps buttons that would appear behind the details of an event

# Case Two

**User:**

* Biology major

* iOS and Apple user

* Told the description of the app and nothing else

**Good:**

* Understood how to navigate the map view

* Identified the pins as events and knew to tap them to get more information

* Use of buttons on the map view were apparent after the first use, but not initailly 

**Bad:**

* Tapping an event on the my events view should do something 

* Wasn’t aware of the sidebar

* Wasn’t aware of the search bar on the map 

* Wasn’t aware that you swipe down to bring the filter/search down 

* Wasn’t aware of how to create a new event

* Wants to see who is attending the event since they may be more likely to attend if they know someone or are friends with someone who is attending

* Wants the ability to delete and modify events

**Conclusions:**

A simple tutorial or help screen is needed for the final release to allow users to utilize all the features of our app since most of the functions of our app aren’t immediately obvious. 

**Improvements:**

* The names of the people attending an event are now visible 

    * With follow-up study after the fix, user wanted to click on the name to bring up information on that user

# Case Three

**User:**

* Chemical Engineering major

* iOS and Apple user.

* Told the purpose of the app and nothing else.

**Good:**

* Able to log in smoothly.

* Able to browse around on the map and find event details by tapping on markers

* Able to attend and unattend events

* Able to go into the list view and apply filters/search.

* Able to locate and use the sidebar: my events, Facebook login/logout.

* Able to tap and hold on map to find the Add Event page and add an event to the map.

**Bad:**

* Thought there was too little information.

* Missing starting hour for event details, only date.

* Input keyboard stayed in map view when going back from the list view.

* MyEvent contains events that has "Attend?" button on the map.

* After logging out, still able to attend events and displayed the logged out user’s name in the attendance.

**Suggestions:**

* Suggested implementing push notifications.

* Suggested displaying address in the Add Event page.

* Suggested integration with weather.

* Suggested indoor/outdoor option for events.

**Conclusion:**

* Needs to display event details in a more robust form.

* The UI of map details and add event needs improvements.

* Push notifications, weather and extra attributes of events are worth thought as stretch goals for this development period.

**Improvements:**

* Added hours to the event details.

* Keyboard is dismissed when entering the Maps view

* Related bug fixes.

