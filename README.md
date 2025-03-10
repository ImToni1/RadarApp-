# UL-Radar

UL-Radar is a project that integrates various sensors and components to monitor and display data using Raspberry Pi. The project includes ultrasonic sensors, a microphone, a motor, LEDs, and an OLED display. The data collected from the sensors is sent to a backend server and displayed on a web interface.

## Struktura Projekta

```
backend/
  ├── models/
  │   └── database.sqlite
  ├── package.json
  ├── public/
  │   ├── icon.png
  │   ├── index.html
  │   ├── script.js
  │   └── style.css
  └── src/
      ├── engine.js
      └── routes.js
pi/
  ├── display.py
  ├── main.py
  ├── microphone.py
  ├── motor.py
  └── ultrasonic.py
README.md
```
## Project Flow

### First Week

The first week we selected team members. Our team consists of:
- Toni Jelavić
- Saša Adamović
- Lovro Broić
- Luka Leon Grubišić

### Second Week

The second week we selected the equipment we needed for the project. The equipment list includes:

- **Servo motor**: [Adafruit Servo Motor](https://www.adafruit.com/product/324)
- **Display**: [Adafruit Display](https://www.adafruit.com/product/326)
- **Motor driver**: [DRV8825 Stepper Motor Driver Module](https://www.amazon.de/dp/B07Q5X5Q8X)
- **Power supply**: [Power supply 36W 12V 3A](https://www.ledshop.rs/napajanje-36w-12v-3a)
- **Digital compass**: [DAOKAI Triple Axis Compass Magnetometer Sensor](https://www.amazon.de/dp/B07Q5X5Q8X)

### Third Week

In the third week, we received the equipment and started connecting all the components.

### Fifth Week

In the fifth week, we started with 3D design and creating a web application.

### Week Six

We finished everything in the sixth week and put everything together in a box. That was the end of the project.

## Backend

The backend is responsible for serving the web interface and handling the storage and retrieval of data. It uses SQLite for the database and Node.js for the server.

## Backend

The backend is responsible for serving the web interface and handling the storage and retrieval of data. It uses SQLite for the database and Node.js for the server.

### Files

- `backend/models/database.sqlite`: SQLite database file.
- `backend/package.json`: Contains project metadata and scripts.
- `backend/public/index.html`: The main HTML file for the web interface.
- `backend/public/script.js`: JavaScript file to handle chart updates and notifications.
- `backend/public/style.css`: CSS file for styling the web interface.
- `backend/src/engine.js`: Contains functions for database operations.
- `backend/src/routes.js`: Defines server routes and handles HTTP requests.

### Pi Files

- `pi/display.py`: Handles the OLED display.
- `pi/main.py`: The main script that integrates all components and sends data to the backend.
- `pi/microphone.py`: Handles microphone input and buzzer output.
- `pi/motor.py`: Controls the motor.
- `pi/ultrasonic.py`: Reads data from ultrasonic sensors.

## Starting Backend

To start the backend server, run the following command:

```sh
npm start
```

## Starting the Pi Instance

To start the Pi instance, run the following command:

```sh
python3 main.py
```

## Features

- **Red Light Status**: Shows the status of the red light.
- **Sound Status**: Shows the status of the sound detected by the microphone.
- **Ultrasonic Sensor Data**: Displays data from two ultrasonic sensors.
- **Notifications**: Displays raw data notifications.

## Addictions

### Backend

- Node.js
- SQLite

### Raspberry Pi

- RPi.GPIO
- requests
- json
- PIL (Pillow)
- adafruit_ssd1306