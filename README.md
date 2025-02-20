# Expo Tabs - Building with Expo's Navigation

## Documentation

* https://docs.expo.dev/router/advanced/tabs/
* https://www.youtube.com/watch?v=D4XAhkjJXD4

## What to Do

**Objective:** Learn to create interactive tabs using React Native and Expo, following Expo's documentation for navigation.

**Instructions:**

1. **Clone this repository:** `git clone https://github.com/felieppe/agrofit-tabs.git`
2. **Navigate to the template folder:** `cd agrofit-tabs`
3. **Install dependencies:** `npm install` or
4. **Start the development server:** `expo start` or `npx expo start`
5. **Implement a fake login:**

   * Create a simple login screen (e.g., `LoginScreen.js`).  This screen should have input fields for email and password and a login button.
   * For this assignment, you don't need to implement real authentication.  Instead, create a mock authentication.  When the user enters any email and password (or specific credentials if you prefer), navigate them to the main tabbed interface.
  
  
6. **Implement the tabs:**

   * **Consult the Expo Navigation Documentation:**  Your primary resource for this assignment is the official [Expo Navigation documentation](https://docs.expo.dev/router/advanced/tabs/).

   * **Create Three Tabs:**  Your app should have three tabs:
      * **Home:** This tab will display a simple welcome message or some basic information.
      * **Explore:** This tab could display a list of items (e.g., categories, locations, etc.)
      * **Profile:** This tab will represent a user profile. A simple greeting like "Hello, [Your Name]" is sufficient.

   * **Implement Tab Navigation:** Use the tab navigation components provided by Expo Navigation.  You'll need to install the necessary packages (refer to the documentation).  Set up the tab navigator to switch between the three tabs you created.

   * **Styling (Basic):** Give the tabs and their content some basic styling.

**Requirements:**

* **Functional Tabs:** The tabs should switch content correctly when pressed.
* **Three Tabs:**  The app must have the three specified tabs (Home, Explore, Profile).
* **Basic Styling:**  The app should have clear and readable styling.
* **Clean Code:**  Write well-formatted and commented code.

**Example (Conceptual - Refer to Expo Documentation for Actual Implementation):**

```javascript
// This is a simplified example.  Consult the Expo Navigation docs for the correct code!
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs'; // From Expo Navigation
import HomeScreen from './screens/HomeScreen';
import ExploreScreen from './screens/ExploreScreen';
import ProfileScreen from './screens/ProfileScreen';

const Tab = createBottomTabNavigator();

export default function App() {
  return (
    <NavigationContainer>  {/* Required for navigation */}
      <Tab.Navigator>
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Explore" component={ExploreScreen} />
        <Tab.Screen name="Profile" component={ProfileScreen} />
      </Tab.Navigator>
    </NavigationContainer>
  );
}

// ... (HomeScreen, ExploreScreen, and ProfileScreen components)
