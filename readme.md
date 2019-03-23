# Clickr Testing Instructions

## Install the Chrome extension

1. Download the zip file and unzip it into a folder on your machine -- you'll probably want to always re-use the same folder as chrome makes it easy to update that way.
1. Go to the chrome settings > manage extensions: chrome://extensions/
1. Click "Load Unpacked" and then pick the folder that you unzipped to (should have 'manifest.json')
1. To refresh/restart the extension (if something goes horribly wrong) you can click the little refresh icon on that extensions page
1. Note: any browser windows you have open prior to installing the extension will need to be refreshed for the app to talk to them.

## Install the Android app

1. Go to the drive link using the android device and download the clickr-android.apk file
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

1. You should be able to use the "CHANGE" button to switch to the "Browser List" page, where you can change your connection to a different browser or reconnect to the current one. (See below for full details on this page)
2. Navigation Controls:
   1. You should be able to use the "&#8592;" to go back in the browser.
   1. You should be able to use the "&#8635;" button next to the textbox to reload the page
   1. You should be able to enter a url into the text box at the top, then click the "go" button (depending on keyboard) and the browser should navigate to the url entered.
   1. This text box should always show the current tab's site url.
   1. You should be able to use the "&#8594;" to go forward in the browser (if you have gone back previously).
3. App browser controls:
   1. Long press on the browser name to open a prompt allowing you to rename it.
   1. Press "change" to open the "Browser List Page" (details below)
4. Text Controls:
   1. You should be able to click "ABC", "123", and "EMAIL" buttons to send text to an input field in the browser.
   1. Depending on your default keyboard app, you should get the corresponding keyboard types from the different buttons.
5. Arrow Controls:
   1. You should be able to tab left/right with the circular left/right arrows and the currently focused element will have a prominent and visible border.
   1. You should be able to move up/down between "sections" on the page with the circular up/down arrows (this is relatively dependent on the site using standardized web accessibility elements OR special code being written in the extension to determine this behavior -- Hulu, Netflix, and Google should be _decent_)
   1. You should be able to Click the focused element with the circular button in the middle of the arrows.
   1. You should be able to use the scroll bar on the right by dragging up or down to scroll the browser window. Swiping quickly should scroll more, dragging precicely should scroll less.
6. You should be able to use the video controls if there is a video element on the page, details below: 1) "PLAY" and "PAUSE" should work as expected. 1) "FULL" should bring the window and video to full screen 1) The "+"/"-" volume controls should work well (it will NOT give any visual indication of the volume changing, but it should actually work).  
    1) **KNOWN ISSUE** The "fast forward" buttons "<<" and ">>" have some problems and can cause errors (Netflix) 1) The draggable slider at the bottom does nothing currently

## Tabs Drawer

1. Clicking the "Tabs" at the bottom of the remote should slide open the tabs drawer. This can also be opened by swiping the remote to the left from the right side of the screen.
1. This should show all of the windows and their tabs currently open in your connected browser. Windows will have a semi-random name based on the nato phonetic alphabet.
1. Tapping the "window +" at the top should open a new browser window.
1. Tapping the "tab +" next to the window name should open a new tab within that window and bring it into focus.
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

1. The browser still needs to inform the remote about information within the current page to get the following functionality: 1) Showing/hiding controls based on what is focused 1) Showing/hiding controls if a video is actively playing 1) Showing (and changing) current location of video with the slider control 1) Give basic video controls in notifications and lock screen when video playing
1. Give visual indication of volume changing
1. Fix above known issues
1. Better UI and/or themes
1. Show ads
