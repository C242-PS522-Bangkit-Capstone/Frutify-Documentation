# **Frutify**

Fruit Scanner App is an Android-based application that utilizes image processing technology to analyze fruits. This app helps users detect fruit conditions, view nutritional content, and save the analysis data.


## **Key Features**
- **Fruit Recognition**: Capture images of fruits to identify their type and condition.
- **Nutritional Information**: Access detailed nutrition facts based on the fruit analysis.
- **Save Analysis Results**: Store analysis data, including images, weight, and date.
- **Fruit Data Management**: Retrieve previously scanned fruit data.
- **Reminder Notifications**: Get alerts to check your fruit’s freshness.



## **System Requirements**
- Android 7.0 (Nougat) or higher.
- Functional device camera.
- Internet connection for image analysis and data retrieval.



## **Installation Guide**

1. Clone this repository:
   ```bash
   git clone https://github.com/username/fruit-scanner-app.git
   ```
2. Open the project in **Android Studio**.
3. Sync dependencies:
   ```bash
   ./gradlew build
   ```
4. Run the app on an emulator or physical device.



## **Technologies Used**
- **Kotlin**: Primary programming language.
- **Jetpack Compose**: For building the user interface (UI).
- **Retrofit**: For API communication.
- **CameraX**: For capturing fruit images.
- **LiveData & ViewModel**: For state and data management.
- **Room Database**: For local data storage.



## **API Endpoints**
The app interacts with a backend API to retrieve and store data.

### **1. Fetch All Scan Data**
- **Endpoint**: `/api/data`
- **Method**: `GET`
- **Response**: 
  ```json
  {
    "error": false,
    "message": "Successfully retrieved data",
    "data": [
      {
        "id": 1,
        "fruitName": "Apple",
        "weight": 150,
        "nutritionInfo": "Calories: 95, Fiber: 4g, Vitamin C: 14%",
        "scanDate": "12 December 2024"
      }
    ]
  }
  ```

### **2. Save Scan Data**
- **Endpoint**: `/api/data`
- **Method**: `POST`
- **Request**:
  ```json
  {
    "fruitName": "Apple",
    "weight": 150,
    "nutritionInfo": "Calories: 95, Fiber: 4g, Vitamin C: 14%",
    "scanDate": "12 December 2024"
  }
  ```
- **Response**:
  ```json
  {
    "error": false,
    "message": "Data saved successfully"
  }
  ```



## **How to Use**
1. **Scan Fruit**: Open the app and point the camera at the fruit you want to scan.
2. **Automatic Analysis**: The app will display information about the fruit, such as its condition and weight.
3. **Save Results**: Tap the "Save" button to store the analysis data on the server.
4. **View Saved Data**: Navigate to the **History** page to view all saved data.



## **App Demo**




## **Contributing**
We welcome contributions to improve this application! 
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Make changes and commit:
   ```bash
   git commit -m "Add new feature"
   ```
4. Submit a pull request to the `main` branch.



## **License**
This project is licensed under the [MIT License](LICENSE).

