Clickr gives you full control over your browser from your phone with an intuitive and simple remote control interface. After installing the Chrome or Firefox extension you can easily connect your phone to your browser and have full control of browsing, watching videos and filling out forms, all from the comfort of your couch.

The app is located at:

Android: https://play.google.com/store/apps/details?id=com.willweb.clicker

iOS: https://apps.apple.com/us/app/streaming-remote-control/id1460043343

Chrome Extension: https://chrome.google.com/webstore/detail/phenknepgmgjafkipebllabgcjjnnkbg/publish-accepted?authuser=0&hl=en

Clickr uses web accessibility standards to allow users to navigate web sites displayed on a monitor or TV, turning your android or iPhone into a highly functional remote control. After installing the extension, a small remote control will appear on your browser's toolbar next to the web site's url. Clicking this will display a large QR code. Next. install and open the app. You will see a large "Scan" button at the bottom. Tap that and scan the QR code in your browser's window. That's it! Your phone is now a remote control that can easily navigate your favorite websites!

More details and issue submission can be found here: https://github.com/wpatter6/clickr

# Clickr Alpha Testing Instructions - v1.2.2

## Install the App

### iOS:

1. Join the test flight by [clicking here](https://testflight.apple.com/join/ESs2Bs97)

### Android:

1. Install from Google Play Store: https://play.google.com/store/apps/details?id=com.willweb.clicker

## Install the Chrome extension

1. Install the extension at https://chrome.google.com/webstore/detail/phenknepgmgjafkipebllabgcjjnnkbg
1. Note: any browser windows you have open prior to installing the extension will need to be refreshed for the app to talk to them.

## Connect app to browser

1. You should initially see steps on how to connect the app to the browser
1. Click "SCAN" and you should be prompted to allow access to device's camera (only happens the first time)
1. QR scanner should appear
1. In the browser, you should see a black remote icon in the top right corner after installing the extension.
1. Clicking the remote icon should show a large QR code.
1. Scan that QR code with the phone.
1. If it scans correctly, you should see a green box appear above the QR code in the extension and your phone app should switch to the "remote" page.
   1. The icon in the corner of the browser should also show a green circle with the number "1" inside it
   1. connecting multiple devices should work as well and show the number connected in this circle.
   1. Expanding the QR code should also show a green box with the device manufacturer and a randomized string.
   1. The device can be disconnected from here by clicking the "unplug" icon next to the device name in the green box.
1. You should immediately be promted to name the browser, with the default being the type of browser followed by a unique random 6 character string in parenthesis.

## Remote Page

1. Navigation Controls:
   1. You should be able to use the "&#8592;" to go back in the browser.
   2. You should be able to use the "&#8635;" button next to the textbox to reload the page
   3. You should be able to enter a url into the text box at the top, then click the "go" button (depending on keyboard) and the browser should navigate to the url entered.
   4. This text box should always show the current tab's site url.
2. App browser controls:
   1. Long press on the browser name to open a prompt allowing you to rename it.
   2. You should be able to use the "CHANGE" button to switch to the "Browser List" page, where you can change your connection to a different browser or reconnect to the current one. (See below for full details on this page)
3. Movement Controls:
   1. You should be able to tab left and right by tapping the left or right sides of the circular direction button, and in the browers, the currently focused element will have a prominent and visible border.
   2. You should be able to move up/down between "sections" on the page with the circular up/down arrows (this is relatively dependent on the site using standardized web accessibility elements OR special code being written in the extension to determine this behavior -- Hulu, Netflix, and Google should be _decent_)
   3. You should be able to Click the focused element with the circular button in the middle of the arrows.
   4. You should be able to use the scroll bar on the right by dragging up or down to scroll the browser window. Swiping quickly should scroll more, dragging precicely should scroll less.
   5. You should be able to use the zoom buttons on the left to zoom in or out on the current browser page.
4. Video controls:
   1. "Play" and "pause" should work as expected. The "play" icon should change when the video starts playing to the pause icon, and vice versa.
   2. The "skip forward/backward" buttons should skip the video ahead or back around 10 seconds per click.
      - **KNOWN ISSUE** The "skip forward" buttons "<<" and ">>" can cause errors, especially on Netflix and Hulu or if content is not buffered
   3. "FULL" should toggle the browser window and/or video to full screen
   4. The keyboard button should open a page with a text input which will allow filling in form fields. Drop down controls should appear in a selectable list. There should be left and right arrows that tab left and right, changing the field that can receive text from the remote. The click and submit buttons should work accordingly as well (assuming web-site functionality behaves in this way).
   5. The VOLUME up/down buttons should work when a video is playing, and display a visual indication of the volume level on the bottom right corner of the screen. -**KNOWN ISSUE** volume display is not visible in full screen mode.
   6. The mute button should mute and unmute the video, also showing the visual volume indication.
   7. The TAB up/down buttons should move to the next or previous browser tab.
5. The bookmarks that are configured to show on the remote should be displayed surrounding the volume/tab buttons accordingly.
   1. Tapping the bookmark should navigate the current tab in your browser to the site.
   2. Long-pressing will bring up a menu to allow re-configuring bookmarks, detailed below in the bookmarks page section.

## Tabs Page

1. Clicking the "Tabs" at the bottom of the remote should open the tabs page.
1. This should show all of the windows and their tabs currently open in your connected browser. Windows will have a semi-random name based on the NATO phonetic alphabet.
1. Tapping the "window +" at the top should open a new browser window.
1. Tapping the "tab +" next to the window name should open a new tab within the currently focused window and if another app on your computer is in focus, it should bring the browser window into focus.
1. You should be able to change to a tab by tapping it in the list.
1. Double tapping a tab should bring it to the front if your browser is behind another application. **KNOWN ISSUE** Sometimes this requires and extra tap or two, and sometimes windows 10 will just show it blinking on the toolbar
1. You should be able to refresh a tab by clicking its "&#8635;" icon
1. You should be able to close a tab by clicking its "X" icon.
1. Closing all of the tabs in a window should close the window.

## Bookmarks Page

1. Clicking the "Bookmarks" button at the bottom of the remote should slide open the bookmarks page.
1. It will be pre-populated with some popular video sites, and a "+" and "open all" buttons at the bottom.
1. Clicking the "+" button should add the currently focused tab's page to the list, showing the page's icon with its title.
1. Tapping the bookmark should redirect the browser to the bookmark.
1. Long pressing the bookmark should open a dialog with the following options:
   1. Open in new tab: should open the bookmark in a new browser tab
   1. Rename: should open a input prompt to give the bookmark a different name
   1. Show on Remote Left: should show the bookmark on the bottom left side of the remote, and if shown, will show a ✔ in the dialog.
   1. Show on Remote Right: should show the bookmark on the bottom right side of the remote, and if shown, will show a ✔ in the dialog.
   1. Delete: should permanently delete the bookmark
1. "Open all" button should open all of the bookmarks into separate tabs

## Browser List Page

1. If you are re-scanning a browser you have already scanned, it should not make a duplicate entry.
1. Long pressing a browser should open a dialog with the following options:
   1. Connect: should try to connect the browser even if offline or already connected (helpful to troubleshoot connection issues)
   2. Rename: should open an input prompt to give the browser a different name
   3. Delete: should permanently delete the browser from the list (after a confirmation prompt)
1. You should be able to press the "?" button to view the connection instructions.
1. The connection list should show a button next to the browsers in the list indicating if the browser is already connected (red) can be connected to (green) or is not online to receive a connection (disabled/grey).
1. You should be able to drag the list downward to cause each item to re-check the browser's availability.

## TODOS

1. Showing/hiding controls if a video is actively playing
2. Showing (and changing) current location of video with the slider control
3. Give basic video controls in notifications and lock screen when video playing
4. Showing/hiding controls based on what is focused
5. Fix above known issues
6. Better UI and/or themes
7. Implement ads

## Known Issues

1. Skip forward/back buttons can be buggy especially if content is not buffered
1. Name of the browser does not immediately update on the remote view
1. Browser will sometimes become unresponsive after long idle periods and will require closing all windows and restarting chrome.
