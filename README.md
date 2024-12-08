# Web-Based Graphical Password Authentication System

#Overview

This project is a web-based graphical password authentication system developed using Flask and Firebase. It provides a more secure and user-friendly alternative to traditional alphanumeric passwords by leveraging graphical patterns. Users select an image of their choice and create a password through click patterns on a customizable grid (2x2 or 3x3).
The system is designed to address common security vulnerabilities, including shoulder surfing, keylogging, and password guessing, while enhancing usability and accessibility.

#Features
Graphical Password Mechanism:
Users can select images and set graphical passwords based on click patterns on a grid.
Supports 2x2 and 3x3 grid sizes for flexibility and customization.

#Secure Storage:

Passwords are securely encrypted using the Fernet encryption algorithm and stored in Firebase Firestore.
User images are uploaded to and managed via Firebase Storage.

#User Authentication:
Handles user signup, login, and authentication via Firebase Authentication.

#Security Measures:

Protects against attacks like shoulder surfing and keylogging.
Temporary account blocking after multiple failed login attempts.

#Custom Hint System:

Users can associate a hint with their graphical password for easier recall.
#Technologies Used
Backend: Flask (Python)
Frontend: HTML, CSS, JavaScript (Jinja templating with Flask)
Database and Storage: Firebase (Authentication, Firestore, Storage)
Encryption: Python's cryptography library (Fernet encryption)
#Installation
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/graphical-password-system.git
cd graphical-password-system
Set up the environment:

#Install dependencies:
Copy code
pip install -r requirements.txt
Ensure Python 3.8 or higher is installed.
Configure Firebase:

Download your Firebase Admin SDK credentials JSON file from the Firebase Console.
Place the file in the project directory and update its path in the Flask initialization:
Copy code
cred = credentials.Certificate('path-to-your-firebase-adminsdk.json')
Run the application:

bash
Copy code
python app.py
Access the application: Open your browser and go to http://localhost:5000.

#How It Works
Signup:

Users provide their email, password, and upload an image.
The image is uploaded to Firebase Storage, and a user account is created in Firebase Authentication.
Set Graphical Password:

Users choose a grid size (2x2 or 3x3) and click on sections of their uploaded image to create a unique password pattern.
The password is encrypted and stored in Firestore.
Login:

Users are presented with their image along with decoys and must select their image.
After selecting the correct image, they enter their graphical password by clicking the correct pattern.
Security:

Accounts are temporarily blocked after multiple failed login attempts to prevent brute force attacks.
#Future Scope
Extend the system for use on mobile platforms (Android/iOS).
Add more grid size options (e.g., 4x4) for enhanced security.
Develop browser extensions for integration with websites like Gmail and Facebook.
Improve user experience with advanced features like password recovery and detailed analytics.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.
