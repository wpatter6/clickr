# Clickr Alpha Testing Instructions - v0.1.2

## Install the Chrome extension

1. Download the zip file and unzip it into a folder on your machine -- you'll probably want to always re-use the same folder as chrome makes it easy to update that way.
1. Go to the chrome settings > manage extensions: chrome://extensions/
1. Click "Load Unpacked" and then pick the folder that you unzipped to (should have 'manifest.json')
1. To refresh/restart the extension (if something goes horribly wrong) you can click the little refresh icon on that extensions page
1. Note: any browser windows you have open prior to installing the extension will need to be refreshed for the app to talk to them.

## Install the Android app

1. Using your android device, tap the APK link under assets [on the releases page](https://github.com/wpatter6/clickr/releases/latest) and download the file
1. It should prompt that you're "not allowed to install apps from this source"
1. It should give you the option to allow it and you can install it and run it, (specifics may be different based on your version of android)

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
   5. You should be able to use the "&#8594;" to go forward in the browser (if you have gone back previously).
2. App browser controls:
   1. Long press on the browser name to open a prompt allowing you to rename it.
   2. You should be able to use the "CHANGE" button to switch to the "Browser List" page, where you can change your connection to a different browser or reconnect to the current one. (See below for full details on this page)
3. Arrow Controls:
   1. You should be able to tab left/right with the circular left/right arrows and the currently focused element will have a prominent and visible border.
   2. You should be able to move up/down between "sections" on the page with the circular up/down arrows (this is relatively dependent on the site using standardized web accessibility elements OR special code being written in the extension to determine this behavior -- Hulu, Netflix, and Google should be _decent_)
   3. You should be able to Click the focused element with the circular button in the middle of the arrows.
   4. You should be able to use the scroll bar on the right by dragging up or down to scroll the browser window. Swiping quickly should scroll more, dragging precicely should scroll less.
4. Video controls:
   1. "Play" and "pause" should work as expected. The "play" icon should change when the video starts playing to the pause icon, and vice versa.
   2. The "skip forward/backward" buttons should skip the video ahead or back around 10 seconds per click.
      - **KNOWN ISSUE** The "skip forward" buttons "<<" and ">>" can cause errors, especially on Netflix and Hulu
   3. "FULL" should toggle the browser window and video to full screen
   4. The keyboard button should open a text input to allow sending text to the browser window
   5. The VOLUME up/down buttons should work when a video is playing, and display a visual indication of the volume level on the bottom right corner of the screen.
   6. The mute button should mute and unmute the video, also showing the visual volume indication.
   7. The TAB up/down buttons should move to the next or previous tab.
   8. The bookmarks that are configured to show on the remote should be displayed surrounding the volume/tab buttons accordingly (see bookmarks drawer section below for details).

## Tabs Drawer

1. Clicking the "Tabs" at the bottom of the remote should slide open the tabs drawer. This can also be opened by swiping the remote to the left from the right side of the screen.
1. This should show all of the windows and their tabs currently open in your connected browser. Windows will have a semi-random name based on the NATO phonetic alphabet.
1. Tapping the "window +" at the top should open a new browser window.
1. Tapping the "tab +" next to the window name should open a new tab within the window and bring it into focus.
1. You should be able to change to a tab by tapping it.
1. Double tapping a tab should bring it to the front if your browser is behind another application. **KNOWN ISSUE** Sometimes this requires and extra tap or two
1. You should be able to refresh a tab by clicking its "&#8635;" icon
1. You should be able to close a tab by clicking its "X" icon.
1. Closing all of the tabs in a window should close the window.

## Bookmarks Drawer

1. Clicking the "Bookmarks" button at the bottom of the remote should slide open the bookmarks drawer.This can also be opened by swiping the remote to the right from the left side of the screen.
1. Initially you should see nothing but a "+" and "open all" buttons at the bottom.
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
