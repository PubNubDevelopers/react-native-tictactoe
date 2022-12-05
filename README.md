# Realtime Tic Tac Toe Game in React Native 

⚠️ This tutorial is out of date: While some information may not be completely up to date, this repository still contains some useful insights into developing a React Native application. You can learn more about how PubNub powers [thousands of customers worldwide](https://www.pubnub.com/customers/) in our [PubNub for Developers](https://www.pubnub.com/developers/) resources. Have suggestions or questions about the content of this post? Reach out to devrel@pubnub.com.

A React Native game that lets players play Tic Tac Toe against each other in this classic childhood game. Any moves the player makes will be seen in realtime by the other player, no matter where they are in the world! [PubNub's React SDK](https://www.pubnub.com/docs/react-native-javascript/pubnub-javascript-sdk) is used to power the realtime infrastructure of the game and to provide a connected shared experience for the players. 

<p align="center">
  <img src="./media/android-ios-game.png " alt="ios/android screenshot of the game" width="410" height="410" />
</p>

## Setup
1) To get started, create your [PubNub account](https://admin.pubnub.com/#/register) to get your Pub/Sub API Keys.
2) You need to enable presence to detect the number of people in the game channel, which prevents having more than two people in a game. To do so, go to your [PubNub Admin Dashboard](https://admin.pubnub.com), click on the Demo Project App, or create a new app for this project, and click on Keyset. Scroll down to Application add-ons and toggle the Presence switch to on. Keep the default values the same.

<p align="center">
  <img src="./media/enable-presence.png" alt="Enable Presence add-on" width="450" height="300" />
</p>

3) Clone the repo.
```bash
git clone https://github.com/PubNubDevelopers/react-native-tictactoe.git
```
4) Open the project in your favorite text editor, such as [VS Code](https://code.visualstudio.com/download) or [Notepad++](https://notepad-plus-plus.org/download/)

5) Go to App.js and replace 'ENTER_YOUR_PUBLISH_KEY_HERE' and 'ENTER_YOUR_SUBSCRIBE_KEY_HERE' with the keys you got from Step 1.

6) You need to install the dependencies and link them to the app. You can do this by running the script that's in the root directory. Make sure to make the script executable first.
```bash
#dependencies.sh
chmod +x dependencies.sh # Execute the script
./dependencies.sh # Run the script
```

7) Type the following command to run the app in the simulator:
```bash
react-native run-ios
```
 - You can also run the app in the emulator, but make sure to have the emulator opened first:
 ```bash
react-native run-android
```

8) To test the app without having to open up another simulator/emulator, you can use the [React version](https://github.com/PubNubDevelopers/react-tutorial-tic-tac-toe.git) of this tic-tac-toe app. The React app is already connected to the React Native app and is ready to play. To get started, clone the React App from the repo.
    ```bash
    git clone https://github.com/PubNubDevelopers/react-tutorial-tic-tac-toe.git
    ```
    - Once you open the project, go to the file Game.js and in the constructor, add the same Pub/Sub keys you used for the React Native app. After, type the following command in the terminal to install the dependencies:
    ```bash
    npm install
    ```
    - To run the app, type the following in the terminal:
    ```bash
    npm run
    ```
    - The app will open in http://localhost:3000 with an empty table and two input fields. The React app will be used to join a channel (Note: The React app is currently set up to only join channels and not create them) and the simulator/emulator will be used to create a room channel.


## Build Your Own Realtime Tic Tac Toe Game in React Native

To learn more about this project or if you want to build this project from scratch, check out the [tutorial](https://www.pubnub.com/blog/multiplayer-mobile-tic-tac-toe-react-native-ios-android-part-one/).
