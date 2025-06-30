# Transaction Payment (xTan) - Official Commercial Mobile App

![Screenshot 2024-08-25 at 06 03 04](https://github.com/user-attachments/assets/66093dcc-8a05-428c-87ca-6a54299ddfbb) ![Screenshot 2024-08-25 at 06 04 42](https://github.com/user-attachments/assets/47ecbc44-613d-465a-9663-9672086b6162) ![Screenshot 2024-08-25 at 06 05 00](https://github.com/user-attachments/assets/387b5eb8-b498-41d7-9782-2e951da82cf4) ![Screenshot 2024-08-25 at 06 05 14](https://github.com/user-attachments/assets/335ff3d7-2c0d-465c-8c9c-21576894fa82) ![Screenshot 2024-08-25 at 06 05 29](https://github.com/user-attachments/assets/9aeeb4da-f6b4-4b7c-9c71-0cb52346eb9a) ![Screenshot 2024-08-25 at 06 05 50](https://github.com/user-attachments/assets/711c9297-b133-426b-a138-c09a85af7734) ![Screenshot 2024-08-25 at 06 06 46](https://github.com/user-attachments/assets/5db5b8e6-32ce-4f38-b72f-61ca9ada65d0) ![Screenshot 2024-08-25 at 06 07 01](https://github.com/user-attachments/assets/d588b03e-5bae-47fa-89b8-b037c6e3bc5c)

---

## Project Summary

**Transaction-Payment (xTan)** is a modern, secure, cross-platform mobile application for managing credit card transactions, expenses, analytics, and notifications. It utilizes the Ionic Framework, Cordova, and AngularJS to deliver a native app experience on iOS and Android. The project demonstrates best practices in hybrid app development, secure data handling, and interactive UI design, making it ideal both as a commercial solution and a learning resource for developers.

**Official page:** [https://gil.gmbh/en/projects/project_06/](https://gil.gmbh/en/projects/project_06/)

---

## Table of Contents

- [Project Summary](#project-summary)
- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [How to Run](#how-to-run)
- [Usage Walkthrough](#usage-walkthrough)
- [Screenshots](#screenshots)
- [Project Details & Functionality](#project-details--functionality)
- [Code Samples & Key Scripts](#code-samples--key-scripts)
- [Important Keywords](#important-keywords)
- [Conclusion](#conclusion)
- [License](#license)

---

## Features

- **Secure Credit Card Data Fetching**: Connects to a backend server to fetch and display credit card details and transactions.
- **Expense Management**: Visualizes expenses with graphs, categorized reports, and detailed transaction breakdowns.
- **Push Notifications**: Receives instant notifications about transactions and critical events.
- **Transaction History**: Provides a searchable, filterable transaction log.
- **Security**: OTP (One-Time Password) system for sensitive actions.
- **Responsive UI**: Mobile-first, touch-optimized design for all devices.
- **Analytics & Reporting**: Graphs and charts for insight into spending patterns.
- **Cross-Platform**: Runs on both iOS and Android.

---

## Project Structure

```
Transaction-Payment--AngularApp/
├── hooks/                  # Cordova build lifecycle scripts
├── resources/              # App icons, splash screens, etc.
├── www/                    # Main application code (AngularJS, HTML, CSS, JS)
│   ├── lib/                # Libraries (e.g., angular-animate)
│   └── ...                 # Other source files and assets
├── config.xml              # Cordova project configuration
├── package.json            # NPM dependencies and scripts
├── README.md               # Project documentation
└── ...                     # Additional configs and files
```

- `www/` is the core of the app, containing all AngularJS modules, controllers, views, and assets.
- `resources/` and `hooks/` are standard for Cordova/Ionic projects, providing platform-specific resources and build lifecycle scripts.

---

## Technologies Used

- **Frontend**: Ionic, Cordova, AngularJS, HTML5, CSS3, JavaScript, TypeScript
- **Backend**: REST API (expected, not included in this repo)
- **Mobile Native**: Swift (iOS), Cordova plugins
- **Data Format**: JSON for all server communications

---

## Getting Started

### Prerequisites

- [Node.js & npm](https://nodejs.org/)
- [Ionic CLI](https://ionicframework.com/docs/cli)
- [Cordova CLI](https://cordova.apache.org/docs/en/latest/guide/cli/)
- [Git](https://git-scm.com/)
- (iOS) macOS with Xcode
- (Android) Android Studio and SDK

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
> **Note:** For iOS, a Mac with Xcode is required.

---

## Usage Walkthrough

1. **Launch App**  
   Open the app on your device or emulator.

2. **Sign In & OTP**  
   Log in with your credentials. Sensitive operations require OTP (One-Time Password) verification.

3. **Dashboard**  
   View credit card balances, recent transactions, and analytics.

4. **Transactions**  
   Browse, filter, and search your transaction history.

5. **Expenses & Reports**  
   Visualize your spending with graphs and categorized reports.

6. **Notifications**  
   Receive push notifications for each transaction or important account event.

7. **Settings**  
   Manage app preferences, notifications, and security.

---

## Screenshots

*(See top of this README for app UI and features screenshots)*

---

## Project Details & Functionality

**xTan** is designed to empower users with robust, secure, and insightful management of their credit card activities:

- **Data Privacy**: All sensitive operations (fetching, transactions) secured with OTP and encrypted communication.
- **Rich Visualizations**: Interactive graphs and charts help users understand spending patterns.
- **Real-Time Updates**: Push notifications provide immediate feedback on account activity.
- **Cross-Platform Support**: Built with Ionic and Cordova for seamless deployment on both Android and iOS.

---

## Code Samples & Key Scripts

Below are example code snippets and patterns you’ll find in this project:

### Example: AngularJS Module Setup

```javascript
angular.module('xtanApp', ['ionic', 'ngAnimate'])
  .controller('TransactionController', function($scope, TransactionService) {
    $scope.transactions = [];
    $scope.fetchTransactions = function() {
      TransactionService.getAll().then(function(data) {
        $scope.transactions = data;
      });
    };
  });
```
---

### Example: Fetching Data from Backend

```javascript
.factory('TransactionService', function($http) {
  return {
    getAll: function() {
      return $http.get('https://api.example.com/transactions')
        .then(response => response.data);
    }
  };
});
```
---

### Example: Displaying Transaction List in AngularJS

```html
<ion-list>
  <ion-item ng-repeat="txn in transactions">
    <span>{{txn.date}}: {{txn.amount | currency}}</span>
    <span class="item-note">{{txn.category}}</span>
  </ion-item>
</ion-list>
```
---

### Example: Sending OTP for Security

```javascript
$scope.verifyOTP = function(otp) {
  $http.post('/api/verify-otp', { otp: otp })
    .then(function(response) {
      if (response.data.success) {
        // proceed with transaction
      }
    });
};
```
---

*For full code, see the `www/` directory, especially controllers, services, and views.*

---

## Important Keywords

- **Ionic**
- **Cordova**
- **AngularJS**
- **HTML5**
- **CSS3**
- **JavaScript**
- **TypeScript**
- **JSON**
- **Push Notifications**
- **OTP**
- **Expense Analytics**
- **Mobile App**
- **Cross-Platform**
- **REST API**

---

## Conclusion

Transaction-Payment (xTan) is a robust commercial and educational project for hybrid mobile app development. It demonstrates best practices in user authentication, secure data transfer, real-time notifications, and interactive data visualization.  
Feel free to explore the source code, adapt components, and use this project as a learning or production foundation!

---

## License

This project is licensed under the Apache License 2.0.  
See the [LICENSE](LICENSE) file for more information.

---

> Happy Coding! 🎉  
> Thank you for using and sharing Transaction-Payment (xTan)!
