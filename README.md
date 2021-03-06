## Fix Slack's icon in Plasma's system tray: <img src="https://user-images.githubusercontent.com/9460504/53523339-da3a9800-3adc-11e9-82a9-0e66528d4e82.png" height="30">  <img src="http://www.omgubuntu.co.uk/wp-content/uploads/2017/07/kde-plasma-logo.png" width="30">

<img src="https://user-images.githubusercontent.com/9460504/53522999-ea9e4300-3adb-11e9-991f-41de972ede4b.png" width="30">

1. Clone this repo. 
`git clone`
2. Navigating into the folder
`cd slack-fix`
3. Run the shell script OR execute the copy command
`./slackfix.sh`
OR
`sudo cp slack-taskbar-* /usr/lib/slack/resources/app.asar.unpacked/src/static/`

### Problem statement

On Plasma desktop environment, the system tray icon for Slack has an issue with system tray icon. The size of it is too big as can be seen in the screenshot.

>#### *Before*
>![screenshot_20190227_204758](https://user-images.githubusercontent.com/9460504/53522128-0dc7f300-3ada-11e9-8f4b-cb78e12984fe.png)

### Problem resolution
This repository has the updated Slack icon with 3 possible states (red for highlight, blue for unread and all white for rest).

![screenshot_20190227_214017](https://user-images.githubusercontent.com/9460504/53522230-394add80-3ada-11e9-9bb5-5a435603f182.png)

This is a personal taste so you can change how it looks, using a image manipulation program. (I used GIMP). There's also a 1600x1600 pixels PNG icon included for ease of editing ([downloaded from freebiesupply](https://freebiesupply.com/logos/new-slack-logo-2019/)). Remember to scale to what size you want. I scaled them to 20x20 pixels for my use case.

>#### *After*
>![screenshot_20190227_210359](https://user-images.githubusercontent.com/9460504/53522185-2801d100-3ada-11e9-9946-b00c61183d7b.png)
>
>![screenshot_20190227_220313](https://user-images.githubusercontent.com/9460504/53522812-7ebbda80-3adb-11e9-97f2-dcdbe82d885f.png)

### Implementation 
Finally, the replacement of icons. There exists a shell script which replaces the old icons with the new ones included in this repo.
You can run `./slackfix.sh` and restart Slack to see the changes.
All this script contains is this copy command.
`sudo cp slack-taskbar-* /usr/lib/slack/resources/app.asar.unpacked/src/static/`

----
**Note**: This issue does not exist when Slack was installed using [Flatpak](https://flathub.org/apps/details/com.slack.Slack).

#### Credit 🏆:
This was inspired form [lgodlewski's Medium article](https://medium.com/@l.godlewski/how-to-fix-slack-icon-in-kde-312383c331a9). It has the old Slack icon so I updated them with the new ones.
