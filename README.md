# TryMart - Android Application (Java + XML)

## 📱 About TryMart
**TryMart** is a modern e-commerce Android application with virtual Augmented Reality (AR) Try-On features. This repository contains the complete implementation for **Assignment 2: Android Application Development**, featuring 7 fully functional activities, input validation, custom layout managers, and alternative resource themes.

---

## 🚀 Implemented Features & Screens

1. **Splash Screen (`SplashActivity`)**:
   - Displays the TryMart logo and app name.
   - Automatically navigates to the Login screen after a 2-second delay using a `Handler`.
   - Built with `ConstraintLayout`.

2. **Login Screen (`LoginActivity`)**:
   - Accepts Email/Username and Password inputs with appropriate `inputType`.
   - Performs input validation for empty fields.
   - Provides explicit `Intent` navigation to **Register**, **Forgot Password**, and **Dashboard**.

3. **Register Screen (`RegisterActivity`)**:
   - Accepts Full Name, Email, Password, and Confirm Password.
   - Validates non-empty fields, email regex format (`Patterns.EMAIL_ADDRESS`), minimum password length (>= 6 chars), and password matching.
   - Built using `LinearLayout`.

4. **Forgot Password Screen (`ForgotPasswordActivity`)**:
   - Accepts user email and validates format.
   - Initiates simulated password recovery and navigates to the **Reset Password** screen via explicit `Intent`.
   - Built using `ConstraintLayout`.

5. **Reset Password Screen (`ResetPasswordActivity`)**:
   - Accepts New Password and Confirm New Password fields.
   - Validates minimum length and password matching.
   - Redirects back to **Login Screen** upon success.

6. **Dashboard Screen (`DashboardActivity`)**:
   - Displays 6 core TryMart modules in a 2-column grid using `GridLayout`:
     - 📷 **AR Try-On Camera**
     - 👓 **Eyewear & Glasses**
     - ⌚ **Watches & Straps**
     - 💄 **Makeup & Cosmetics**
     - 👔 **Clothing & Apparel**
     - 🛒 **Cart & Orders**
   - Header with greeting and navigation to **Profile Screen**.

7. **Profile Screen (`ProfileActivity`)**:
   - Displays user info (Name, Email, Phone, Membership status).
   - Provides a **Logout** button that clears the activity backstack and returns to the Login screen.

---

## 🛠️ Technical Highlights
- **Languages & Frameworks**: Java, Android SDK (Min SDK 24 / Target SDK 37), Material Design 3.
- **Layout Managers Demonstrated**:
  - `ConstraintLayout` (`SplashActivity`, `LoginActivity`, `ForgotPasswordActivity`, `ProfileActivity`)
  - `LinearLayout` (`RegisterActivity`, `ResetPasswordActivity`)
  - `GridLayout` (`DashboardActivity`)
- **Resource Management**:
  - `res/values/strings.xml`: Centralized string resources for all UI text.
  - `res/values/colors.xml`: Default light theme palette.
  - `res/values-night/colors.xml`: Alternative dark mode theme palette.
- **Intents**: Explicit `Intent` navigation between all 7 activities.

---

## 🗺️ Navigation Flow
```
[SplashActivity] (2s Delay)
       ↓
[LoginActivity] ───(Click Register)───> [RegisterActivity]
       │
       ├───(Click Forgot Password)───> [ForgotPasswordActivity] ───> [ResetPasswordActivity] ───> [LoginActivity]
       │
       └───(Login Success)───> [DashboardActivity] ───(Click Profile)───> [ProfileActivity] ───(Logout)───> [LoginActivity]
```

---

## 👨‍💻 Author & Repository Info
- **Project Name**: TryMart
- **Course**: Android Application Development (Java + XML) - Assignment 2
