# Workout App Kotlin

Workout App Kotlin is a mobile application built with Kotlin that allows users to explore and track different workout exercises, get a list of recipes according to a range of calories chosen by the user, and calculate their BMI. The app provides a user-friendly interface for browsing exercise details, including targeted body parts, required equipment, and animated GIFs demonstrating the exercises.

## Features

- Browse a wide range of workout exercises.
- Get a list of recipes based on a calorie range you select.
- Calculate your BMI according to your height and weight.
- View exercise details, including name, body parts targeted, equipment required, and animated GIFs.
- Track your workout progress and mark completed exercises.
- Customize your workout routine and create personalized exercise lists.
- User-friendly interface with smooth navigation and intuitive design.

## Screenshots


https://github.com/maorshriki/workout_app_kotlin/assets/74913575/f2f5f706-a87a-4725-9616-f7f99d6dd5d1


## Technologies Used

- Kotlin - The primary programming language for developing the Android application.
- Android Jetpack - A suite of libraries and tools providing components and architectural guidance for building robust Android apps.
  - ViewModel - Manages and retains UI-related data across configuration changes.
  - LiveData - Observable data holder that notifies views of any changes.
  - Room - Provides an abstraction layer over SQLite for local data persistence.
  - RecyclerView - Displays large sets of data efficiently in a scrollable list.
- OkHttp - A powerful HTTP client for making network requests.
- Glide - An image loading and caching library for displaying GIF animations and images.
- JSON - Parsing and handling JSON data received from the API.
- RapidAPI - Integration with RapidAPI platform for accessing workout exercise data, recipes data, and BMI.

## Installation

1. Clone the repository: `git clone https://github.com/your-username/workout_app_kotlin.git`
2. Open the project in Android Studio.
3. Build and run the application on an Android emulator or physical device.


## API Integration
 * The app is written in Kotlin and leverages Hilt for dependency injection.
 * It interacts with multiple APIs to provide features related to workouts,
 * diet menus, and BMI calculation. The app uses the Retrofit library to handle API calls.

### Required Configuration:
 * Before running the app, you need to set up your API key.
 * This key is used for all the APIs accessed by the app.
 *
 * 1. The API key is retrieved through the ApiKey object located in the com.example.myapplication.utils.ApiKey package.
 *    Replace the existing API key with yours:
 *    
 *    private const val apiKey: String = "YOUR_API_KEY"

 *
 * 2. The API key is then accessed in the NetworkModule to provide headers for all the API calls made through Retrofit.
 *    If you have set the API key correctly, you don't need to change anything in the NetworkModule.
 *    
 *    private var apiKey: String? = null
 *
 *    @Provides
 *    @Singleton
 *    fun provideApiKey(): String {
 *        if (apiKey == null) {
 *            apiKey = ApiKey.getApiKey()
 *        }
 *        return apiKey!!
 *    }
 
### APIs Used:
 * ----------
 * 1. Workout API: Fetches exercise data from the RapidAPI platform.
 *    The API is accessed through the WorkoutApiService interface.
 *
 * 2. Menu API: Provides keto diet menu options from the RapidAPI platform.
 *    The API is accessed through the MenuApiService interface.
 *
 * 3. BMI API: Provides BMI calculations from the RapidAPI platform.
 *    The API is accessed through the BMIApiService interface.
 * Each API service is set up as a singleton via Hilt's @Singleton annotation and is provided
 * through separate methods in the NetworkModule.
 */


## Contributions

Contributions to the Workout App Kotlin are welcome! If you find any bugs or want to enhance the app with new features, feel free to open issues and submit pull requests.

Before contributing, please review the [Contributing Guidelines](CONTRIBUTING.md) for more information.

---

We hope you enjoy using the Workout App Kotlin! If you have any questions or need assistance, please contact us
