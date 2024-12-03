# Home Security System with RFID and Multi-factor Authentication  

---

## Overview  

This project introduces a **secure and user-friendly home security system** that employs RFID technology and multi-factor authentication. By integrating an RC522 RFID card reader, R307 fingerprint sensor, and numerical password entry, we provide robust access control. A **mobile application** enhances the user experience, allowing access management, log monitoring, and temporary passkey generation.  

---

## Features  

### **Hardware Components**  
- **RC522 RFID Reader and Tag**: RFID-based authentication for user identification.  
- **R307 Fingerprint Sensor**: Adds biometric verification for enhanced security.  
- **Keypad**: Enables numerical password entry for additional flexibility.  
- **ESP32 Microcontroller**: Manages hardware operations and communicates with the mobile app.  
- **Buzzer**: Provides audio feedback:  
  - Single beep: Successful authentication  
  - Double beep: Failed authentication  
- **LED Indicators**:  
  - Blue LED: Successful authentication  
  - Red LED: Failed authentication  
- **Servo Motor**: Secures the locking mechanism.  

### **Software Components**  
- **Flutter Framework**: Used to develop the mobile app for managing accounts, access logs, and passkey generation.  
- **Firebase Backend**: Handles authentication, database storage, and real-time syncing with hardware.  

---

## System Workflow  

1. **Authentication Process**  
   - **Step 1**: User scans their RFID card.  
   - **Step 2**: If valid, the system requests fingerprint verification.  
   - **Optional**: A numerical password can also be entered using the keypad.  
   - **Feedback**:  
     - Success: Blue LED and one beep.  
     - Failure: Red LED and two beeps.  

2. **Mobile App Features**  
   - View logs of successful and failed access attempts.  
   - Generate and manage temporary passkeys valid for 10 minutes.  
   - Real-time sync with Firebase for secure and seamless access control.  

3. **Real-Time Logging**  
   - All access attempts are logged in Firebase for transparency.  
   - Logs include RFID scans, fingerprint matches, and password entries.  

4. **Lock Control**  
   - Successful authentication triggers the servo motor to unlock the door.  
   - Hardware feedback ensures user awareness of the process outcome.  

---

## Mobile Application  

Built using the **Flutter Framework**, the app provides an intuitive interface for seamless interaction:  
- **Login and Signup**: Securely create and manage accounts.  
- **Access Logs**: Monitor successful and failed access attempts with timestamps.  
- **Temporary Passkeys**: Generate one-time passwords for guests without RFID cards or registered fingerprints.  

---

## Future Enhancements  

To further improve the system, we propose:  
1. **Camera Integration**: Capture images during each access attempt for visual verification.  
2. **Geo-Fencing**: Restrict access based on the user’s geographic location.  
3. **Push Notifications**: Provide real-time alerts for all access attempts.  
4. **IoT Integration**: Expand functionality to control other smart home devices, such as lights and cameras.  

---

## Installation and Usage  

### **Hardware Setup**  
1. Connect the RFID reader, fingerprint sensor, keypad, and servo motor to the ESP32 microcontroller.  
2. Install the buzzer and LED indicators for feedback.  

### **Software Setup**  
1. Clone this repository:   
2. Install required dependencies for Flutter and Firebase:  
3. Deploy Firebase backend and configure it to sync with the mobile app.  
4. Upload the microcontroller code to the ESP32.  

### **Run the System**  
1. Power the hardware components.  
2. Use the mobile app for access management and monitoring.  

---

## References  

1. **ESP32**: [Introduction to ESP32](https://www.electronicwings.com/esp32/introduction-to-esp32)  
2. **Fingerprint Sensor**: [Biometric Door Lock System](https://iotprojectsideas.com/esp32-based-biometric-door-lock-system-using-r307-fingerprint-sensor-blynk-iot)  
3. **RFID**: [RC522 Interfacing with ESP32](https://www.electronicwings.com/esp32/rfid-rc522-interfacing-with-esp32)  

---

## Conclusion  

This project successfully integrates **multi-factor authentication** with robust hardware and software design, offering a secure and scalable solution for modern home security needs. Future advancements like IoT integration and geo-fencing can make the system even more versatile and effective.