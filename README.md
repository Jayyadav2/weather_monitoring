# Weather Monitoring Application Documentation
Overview
A web application that provides current weather data and daily weather summaries for specified cities. This project utilizes a Spring Boot backend and a React frontend.

Table of Contents
Features
Technologies
Getting Started
Running the Application
Building the Application
API Endpoints
Usage
License
Features
Fetch current weather data for a specific city.
Retrieve daily weather summaries including average, max, and min temperatures.
Responsive and user-friendly interface.
Technologies
Frontend: React, Axios, CSS
Backend: Spring Boot, Java
Database: MySQL (for storing historical weather data)
APIs: OpenWeatherMap API (for fetching weather data)
Getting Started
Prerequisites
Java 11 or higher
Node.js (v14 or higher)
MySQL
Maven
Setup Instructions
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/weather-monitoring.git
cd weather-monitoring
Backend Setup:

Navigate to the backend directory:
bash
Copy code
cd backend
Configure your application.properties file with your MySQL database details.
Running the Application
Run the Spring Boot Application:

You can run the Spring Boot application using the following command:

bash
Copy code
mvn spring-boot:run
This command starts the application and makes it accessible at http://localhost:8080.

Note: Ensure that your MySQL database is running and properly configured in application.properties.
Building the Application
If you want to build the backend application into a JAR file, use the following command:

bash
Copy code
mvn clean package
This command will create a JAR file in the target directory. You can run the generated JAR file using:

bash
Copy code
java -jar target/weather-monitoring-0.0.1-SNAPSHOT.jar
Make sure to replace weather-monitoring-0.0.1-SNAPSHOT.jar with the actual name of the generated JAR file, if it differs.

Frontend Setup
Navigate to the frontend directory:

bash
Copy code
cd ../frontend
Install dependencies:

bash
Copy code
npm install
Start the development server:

bash
Copy code
npm start
The frontend will be available at http://localhost:3000.

API Endpoints
Current Weather
GET /api/weather/current/{city}

Response:

json
Copy code
{
    "main": {
        "temp": 26.31,
        "feels_like": 26.31,
        "temp_min": 26.31,
        "temp_max": 26.31
    },
    "weather": [
        {
            "main": "Clear",
            "description": "clear sky"
        }
    ],
    "dateTime": "1970-01-01 05:30:00"
}
Weather Summary
GET /api/weather/summary/{city}

Response:

json
Copy code
{
    "id": 7,
    "averageTemp": 26.22,
    "maxTemp": 26.22,
    "minTemp": 26.22,
    "dominantWeather": "Clear",
    "city": "Kanpur",
    "date": "2024-10-17"
}
Usage
Open the application in your web browser at http://localhost:3000.
Enter a city name to fetch the current weather and weather summary.
View the displayed weather information.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Note:
Feel free to save this document as README.md or any format that suits your project. You can further customize it with specific details, examples, or instructions as needed! If you need any changes or additions, let me know!
