# 💪 BulkUp - Gym Equipment E-Commerce App

![Android](https://img.shields.io/badge/Platform-Android-green?logo=android)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-purple?logo=kotlin)
![Firebase](https://img.shields.io/badge/Backend-Firebase-orange?logo=firebase)
![Razorpay](https://img.shields.io/badge/Payment-Razorpay-blue)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

BulkUp is a full-featured Android e-commerce application for gym equipment shopping. Built with Kotlin and Firebase, it provides a seamless shopping experience from browsing products to placing orders with multiple payment options.

---

## 📱 Screenshots

> *(Add your app screenshots here)*

| Home Screen | Product Detail | Cart | Payment |
|---|---|---|---|
| ![Home](screenshots/home.png) | ![Detail](screenshots/detail.png) | ![Cart](screenshots/cart.png) | ![Payment](screenshots/payment.png) |

---

## ✨ Features

- 🏠 **Home Screen** — Categories, Featured Products, Best Sellers
- 🔍 **Product Search** — Search across all gym equipment
- 📦 **Product Detail** — Ratings, descriptions, quantity selection
- 🛒 **Cart Management** — Add, update quantity, remove items
- 📍 **Address Management** — Add and select delivery addresses
- 💳 **Multiple Payment Options**
  - Cash on Delivery
  - UPI (PhonePe, Google Pay, Manual UPI ID)
  - Card Payment (Razorpay + Manual card form)
- 📋 **Order Summary** — Review orders before placing
- ✅ **Order Tracking** — View past orders
- 🔐 **Authentication** — Login & Signup with Firebase Auth

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| **Kotlin** | Primary programming language |
| **Android SDK** | Mobile app development |
| **Firebase Firestore** | Real-time NoSQL database |
| **Firebase Authentication** | User login & signup |
| **Razorpay SDK** | Payment gateway integration |
| **ViewBinding** | View management |
| **RecyclerView** | Product listings |
| **CardView** | UI components |
| **Material Design** | UI/UX design system |

---

## 🏗️ Project Structure

```
com.example.bulkup
├── Adapter
│   ├── BestSellerAdapter.kt
│   ├── CategoryAdapter.kt
│   ├── FeaturedAdapter.kt
│   ├── CartItemAdapter.kt
│   └── MyOrdersAdapter.kt
├── model
│   ├── Equipment.kt
│   ├── Category.kt
│   ├── Order.kt
│   └── SelectedAddress.kt
├── HomeActivity.kt
├── HomeFragment.kt
├── ProductDetailActivity.kt
├── CartActivity.kt
├── SelectAddressActivity.kt
├── AddAddressActivity.kt
├── PaymentActivity.kt
├── OrderSummaryActivity.kt
├── OrderSuccessActivity.kt
├── MyOrdersActivity.kt
├── LoginActivity.kt
├── SignupActivity.kt
└── SplashActivity.kt
```

---

## 🔥 Firebase Collections

```
Firestore Database
├── Category/          → Product categories
├── Featured/          → Featured products
├── BestSeller/        → Best selling products
├── AllProducts/       → All gym equipment
├── Users/
│   ├── Cart/          → User's cart items
│   ├── Addresses/     → Delivery addresses
│   └── Orders/        → User's orders
└── Orders/            → All orders
```

---

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog or later
- Android SDK 24+
- Firebase account
- Razorpay account (for payments)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/YourUsername/BulkUp.git
cd BulkUp
```

2. **Set up Firebase**
   - Go to [Firebase Console](https://console.firebase.google.com)
   - Create a new project
   - Add Android app with package name `com.example.bulkup`
   - Download `google-services.json`
   - Place it in the `app/` directory

3. **Set up Razorpay**
   - Go to [Razorpay Dashboard](https://dashboard.razorpay.com)
   - Get your API Key
   - Replace `YOUR_RAZORPAY_KEY_ID` in `PaymentActivity.kt`

4. **Build and Run**
   - Open project in Android Studio
   - Sync Gradle files
   - Run on emulator or physical device

---

## 📋 Firestore Security Rules

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /Category/{id} { allow read: if true; allow write: if request.auth != null; }
    match /Featured/{id} { allow read: if true; allow write: if request.auth != null; }
    match /BestSeller/{id} { allow read: if true; allow write: if request.auth != null; }
    match /AllProducts/{id} { allow read: if true; allow write: if request.auth != null; }
    match /Users/{userId}/{document=**} { allow read, write: if request.auth != null; }
    match /Orders/{orderId} { allow read, write: if request.auth != null; }
  }
}
```

---

## 👩‍💻 Developer

**Madhumitha**
- 📧 Email: your.email@gmail.com
- 💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- 🐙 GitHub: [github.com/yourusername](https://github.com/yourusername)

---

## 📄 License

```
Copyright 2026 Madhumitha

Licensed under the Apache License, Version 2.0
```

---

⭐ **If you like this project, please give it a star!** ⭐
