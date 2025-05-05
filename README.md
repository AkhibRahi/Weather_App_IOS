**Weather App (React Native – iOS)**
A sleek and modern Weather App for iOS, built using React Native. The app fetches and displays real-time weather data for any city, with support for light/dark modes, dynamic styling, and clean architecture using Redux Toolkit and Context API.

**Features**
Search weather by city name
Display current weather info (temperature, humidity, weather type)
Dark and light theme support
Dynamic UI styling with Context
iOS optimized layout and icons
Reusable and modular component design
Stores last searched city using persistent state
Singleton pattern for API management
Unit testing (basic coverage)



**My Approach**
**Architecture**: Followed a clean and modular architecture by separating API logic, components, contexts, and Redux slices.
**Theme Management**: Integrated system preference detection using Appearance.getColorScheme along with a manual theme toggle via Redux Toolkit.
**State Management**: Used Redux Toolkit for global theme state and AsyncStorage to persist the last searched city even after the app restarts.
**API Integration**: Managed via a Singleton class, ensuring centralized and reusable API logic.
**Reusable Components**: Designed small, scalable, and self-contained components for easier maintenance.
**UI/UX**: Focused on simplicity and consistency, ensuring proper iOS design compliance.

**API Used**
OpenWeatherMap API : https://openweathermap.org

**State Management**
Utilized Redux Toolkit for managing theme state and city search state.
AsyncStorage is used to store and retrieve the last searched city so that it's displayed when the app is reopened.
Easy to switch to React Context if needed, as the architecture is modular.

**Folder structure**:
src/
├── api/             # Singleton API class
├── components/      # Reusable UI components
├── contexts/        # Theme context
├── redux/           # Redux slices and store
├── screens/         # App screens
└── utils/           # Utility/helper functions

Code follows best practices for readability and maintainability.
Well-commented logic, clean and understandable structure.

**Testing**
Unit tests implemented for core components and logic.
**Tools used**: @testing-library/react-native and jest.

**Bonus Feature**
Dark Mode Toggle
Users can manually switch between light and dark themes, or let the app auto-detect system theme using useColorScheme.

**Setup Instructions (iOS)**
1. **Clone the Repository**:
git clone https://github.com/yourusername/weather-app-ios.git
cd weather-app-ios
2. **Install Dependencies**
npm install
# or
yarn install
3. **Add .env File**
Create a .env file in the root directory:
WEATHER_API_KEY=your_api_key_here

4. **Install iOS Dependencies (CocoaPods)**
Make sure you're in the root project directory, then:
cd ios
pod install
cd ..
Note: You must run pod install before launching on iOS.

5. **Run the App on iOS**
Start the Metro Bundler:
npm start
# or
yarn start
In a new terminal, run:
npm run ios
# or
yarn ios

**Troubleshooting (iOS)**
Run pod install again if native dependencies change
Reset Metro cache:
npx react-native start --reset-cache

Simulator issues? Clean the build:
cd ios && xcodebuild clean && cd ..


