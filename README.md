# Transaction-Payment (Official Commercial Mobile App)

![Screenshot 2024-08-25 at 06 03 04](https://github.com/user-attachments/assets/66093dcc-8a05-428c-87ca-6a54299ddfbb)

![Screenshot 2024-08-25 at 06 04 42](https://github.com/user-attachments/assets/47ecbc44-613d-465a-9663-9672086b6162)

![Screenshot 2024-08-25 at 06 05 00](https://github.com/user-attachments/assets/387b5eb8-b498-41d7-9782-2e951da82cf4) ![Screenshot 2024-08-25 at 06 05 14](https://github.com/user-attachments/assets/335ff3d7-2c0d-465c-8c9c-21576894fa82) 

![Screenshot 2024-08-25 at 06 05 29](https://github.com/user-attachments/assets/9aeeb4da-f6b4-4b7c-9c71-0cb52346eb9a) ![Screenshot 2024-08-25 at 06 05 50](https://github.com/user-attachments/assets/711c9297-b133-426b-a138-c09a85af7734) 

![Screenshot 2024-08-25 at 06 06 46](https://github.com/user-attachments/assets/5db5b8e6-32ce-4f38-b72f-61ca9ada65d0) ![Screenshot 2024-08-25 at 06 07 01](https://github.com/user-attachments/assets/d588b03e-5bae-47fa-89b8-b037c6e3bc5c)

---

## Project Overview

**Transaction-Payment** (xTan) is a commercial-grade mobile application designed to securely fetch, display, and manage credit card transactions and expenses. The app leverages modern web and mobile technologies to offer a seamless, intuitive, and secure experience for users seeking to track their financial activities.

Visit the official project webpage: [https://gil.gmbh/en/projects/project_06/](https://gil.gmbh/en/projects/project_06/)

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [How to Run](#how-to-run)
- [Usage Walkthrough](#usage-walkthrough)
- [Screenshots](#screenshots)
- [Project Details & Functionality](#project-details--functionality)
- [Keywords](#keywords)
- [License](#license)

---

## Features

- **Secure Credit Card Data Fetching:** Connects to a backend server to fetch and display credit card details.
- **Expense Management:** Visualizes expenses with graphs and reports.
- **Push Notifications:** Receives timely notifications about transactions and important events.
- **Transaction History:** Detailed history of all transactions with filter and search options.
- **Security:** OTP (One-Time Password) system for transaction verification and enhanced security.
- **Responsive UI:** Mobile-first design, optimized for both iOS and Android devices.
- **Analytics & Reporting:** Graph-based expenditure analysis, category-wise breakdown, and summary reports.

---

## Project Structure

```
Transaction-Payment--AngularApp/
├── hooks/                  # Cordova hooks for build lifecycle
├── resources/              # App icons, splash screens, etc.
├── www/                    # Main application code (AngularJS, HTML, CSS, JS)
│   ├── lib/                # Libraries (e.g., angular-animate)
│   └── ...                 # Other source files and assets
├── config.xml              # Cordova project configuration
├── package.json            # NPM dependencies and scripts
├── README.md               # Project documentation and images
└── ...                     # Additional configs and files
```

---

## Technologies Used

- **Frontend:** Ionic, Cordova, AngularJS, HTML5, CSS3, JavaScript, TypeScript
- **Backend:** (Assumed) REST API for credit card data (not included in this repo)
- **Mobile:** Swift (for iOS builds), Cordova plugins
- **Data Format:** JSON (for server communication)

---

## Getting Started

### Prerequisites

- [Node.js & npm](https://nodejs.org/)
- [Ionic CLI](https://ionicframework.com/docs/cli)
- [Cordova CLI](https://cordova.apache.org/docs/en/latest/guide/cli/)
- [Git](https://git-scm.com/)
- (For iOS) macOS with Xcode
- (For Android) Android Studio and SDK

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/arnobt78/Transaction-Payment--AngularApp.git
   cd Transaction-Payment--AngularApp
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Install platforms:**
   ```bash
   ionic cordova platform add ios
   ionic cordova platform add android
   ```

---

## How to Run

### In Browser (Development)

```bash
ionic serve
```

### On Android Device/Emulator

```bash
ionic cordova run android
```

### On iOS Device/Simulator

```bash
ionic cordova run ios
```

> Note: For iOS development, a Mac with Xcode installed is required.

---

## Usage Walkthrough

1. **Launch App**  
   Open the app on your device or emulator.

2. **Sign In & OTP**  
   Authenticate with your account. For sensitive operations, OTP (One-Time Password) verification is used to enhance security.

3. **Dashboard**  
   View a summary of your credit card balances, recent transactions, and analytics.

4. **Transactions**  
   Browse your transaction history, filter by date or category, and view detailed reports.

5. **Expenses & Reports**  
   Visualize your spending habits using graphs and categorized reports.

6. **Notifications**  
   Stay updated with push notifications for every new transaction or critical account event.

7. **Settings**  
   Configure app preferences, notification settings, and account security options.

---

## Screenshots

*(The following screenshots are retained from the original README and demonstrate app UI and features. DO NOT DELETE!)*

---

## Project Details & Functionality

**xTan** is built for users who want a comprehensive yet secure way to manage their credit card activities:
- **Data Privacy:** All sensitive operations are protected via OTP and secure server communication.
- **Rich Visualizations:** Graphs and charts help users better understand their spending patterns.
- **Real-time Updates:** Push notifications keep users instantly informed about account activity.
- **Cross-Platform:** Runs smoothly on both Android and iOS, thanks to Ionic and Cordova.

---

## Keywords

Using Ionic, Cordova, AngularJS, HTML, CSS, JSON, JavaScript, Swift, TypeScript

---

## License

This project is licensed under the Apache License 2.0.  
See the [LICENSE](LICENSE) file for more information.

---
