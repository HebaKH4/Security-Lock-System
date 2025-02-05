# Security Lock System
The Security Lock System is an embedded solution designed to provide secure, convenient access to homes. Built around an Arduino Mega microcontroller, it integrates a motion sensor for activity detection, a user-friendly keypad that only activates when motion is detected to save energy, and an LCD for interaction. A servo motor controls the sliding lock mechanism, while Bluetooth communication via an HC-05 module links the system to a website built with Flask for remote control and real-time notifications. The system generates unique activation codes for secure re-entry, which are stored securely in Redis, and logs activities for added security. This smart solution offers peace of mind, eliminating the hassle of misplaced keys or unauthorized access.

## Features

- **Remote Control**: Control lock functions from a simple web interface built using Flask.
- **Real-time Notifications**: Get updates on activation codes, security events, and access logs via Socket.IO.
- **Activation Code Storage**: Generated activation codes are securely stored in Redis for re-entry.
- **Command Support**: Send commands to turn off the buzzer, light, or update passcodes.
- **Integration with Arduino**: The system is powered by an Arduino and uses Bluetooth communication (HC-05 module) to interact with the website.

## Technologies Used

- **Arduino**: The embedded system managing the lock mechanism and sensors.
- **Flask**: Web framework for building the control panel.
- **Socket.IO**: Real-time communication for notifications and updates.
- **Redis**: Secure storage of activation codes.
- **HTML/CSS/JavaScript**: Frontend for the user interface.
- **HC-05 Bluetooth Module**: For communication between the Arduino and Flask web app.

## Setup

### Prerequisites

- Python 3.x
- Flask
- Redis
- Socket.IO (for real-time communication)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/emannjoum/Security-Lock-System.git
   ```

2. Install required Python libraries

3. Set up Redis server (local or remote).

4. Upload the Arduino code to your Arduino board (see the `arduino_code` directory).

5. Run the Flask app:
   ```bash
   python app.py
   ```

6. Open the website in your browser at `http://127.0.0.1:5000/`.

## Usage

- Access the control panel via the provided Flask web interface.
- Monitor activation codes and security events.
- Send commands (turning off the buzzer, updating passcodes) through the interface.
