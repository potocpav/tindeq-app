# Workouts App

**This app is work-in-progress, and I don't know how far I'll get before I get bored of it. It is now useful to me, and I use it every day. But YMMV (-:**

This app enables you to track your workouts, habits, body measurments, or other values.


## Features

- **Multiple Workout Tracking**: Track any type of workout data with customizable units and values
- **Flexible Data Visualization**: Analyze your progress with interactive charts, including box plots, line graphs, and histograms
- **Simple and Intuitive**: Clean interface focused on quick data entry and easy analysis
- **Smart Organization**: Tag your workouts and filter data to focus on what matters to you

## ToDo List

In order to make this app a full-featured management app for workout data, the following list of features must be implemented:
  
### Features

* [x] Graph settings persistence
* [ ] Implement editing composite units
* [ ] Allow value-less goals
* [ ] Dragging stat values in Summary page
* [ ] Use the first summary value in Goals.tsx
* [ ] Dragging points in Day View

### Bugs

* [ ] When editing points, preserve their position within a day
* [ ] Fix direct date input
* [ ] Fix localization (date display)
* [ ] Update event filters in Summary page (summaries, calendar, graph)
  * [ ] when goal tags change
  * [ ] when goal unit changes

### General Usability

* [ ] Polish stat editing and dragging
* [ ] Screen orientation & responsive design tweaks
* [ ] Show measurement comments somewhere
* [ ] Show numbers on bar charts
* [ ] Limit graph Panning on the left
* [ ] Make bounds on graphs pixel-perfect
* [ ] Prevent future & far past point input
* [ ] Add week start customization to Settings
* [ ] Performance testing & enhancements
  * [ ] Many points (10k)
  * [ ] Wide date ranges (100 years)

### Publication

* [ ] Rebrand to "Activities" / "Activity Tracker"
* [ ] Add screenshots
* [ ] Make app store description
* [ ] Improve GitHub README
* [ ] Link to GitHub from Settings
* [ ] Rename GitHub project

### Tindeq analysis

* [ ] Remove Tindeq permissions, if I decide against supporting Tindeq device
* [ ] Auto-analyze and add reps from Tindeq
* [ ] Integrate Tindeq with goal management
* [ ] Improve connection so that we never get stuck
* [ ] Tare with automatic disconnect/connect

## Screenshots

[![Screenshot 1](screenshots/sshot-1.thumb.jpg)](screenshots/sshot-1.jpg)
[![Screenshot 2](screenshots/sshot-2.thumb.jpg)](screenshots/sshot-2.jpg)
[![Screenshot 3](screenshots/sshot-3.thumb.jpg)](screenshots/sshot-3.jpg)
[![Screenshot 4](screenshots/sshot-4.thumb.jpg)](screenshots/sshot-4.jpg)
[![Screenshot 5](screenshots/sshot-5.thumb.jpg)](screenshots/sshot-5.jpg)
[![Screenshot 6](screenshots/sshot-6.thumb.jpg)](screenshots/sshot-6.jpg)


## Prerequisites

- Expo CLI
- Optional: Tindeq Progressor device

## Running the App

1. **Start the development server**
   ```bash
   npx expo start --tunnel
   ```

2. **Connect your device**
   - Scan the QR code with Expo Go (Android)
   - Scan the QR code with Camera app (iOS)

3. **Grant permissions**
   - Allow Bluetooth permissions when prompted
   - Allow location permissions (required for BLE scanning)

## Usage

### Connecting to a Device

1. **Open the app** and navigate to the main screen
2. **Tap "Connect"** in the status bar
3. **Ensure your Tindeq Progressor** has a blinking green light
   - If not blinking, press the button on the device
4. **Select your device** from the list of available Progressor devices
5. **Wait for connection** - the status indicator will turn green when connected

### Taking Measurements

1. **Navigate to "Live View"** from the main screen
2. **Tare the scale** (optional) by pressing the "Tare" button
3. **Start measurement** by pressing the "Start" button
4. **Perform your exercise** - the app will display real-time data
5. **Stop measurement** by pressing the "Stop" button

## Technical Details

### Architecture

- **State Management**: Zustand for global state
- **Bluetooth**: react-native-ble-plx for BLE communication
- **Charts**: Victory Native for data visualization
- **UI Framework**: React Native with custom styling

## License

This project is licensed under the MIT License
