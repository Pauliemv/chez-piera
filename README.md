# chez-piera - Hotel & Restaurant Management Application for The Scenic Place Resort

This application is a comprehensive hotel and restaurant management solution specifically tailored for Chez Piera at The Scenic Place Resort. It consists of two main components designed to streamline operations and enhance the guest experience:

## Key Features:

**1. Staff Mobile Application (React Native - Native Build):**

* Designed for internal staff use.
* Downloadable from an internal store or sideloaded via Expo/CodePush.
* Functionalities include:
    * Guest Check-in and Check-out
    * Room Assignment Management
    * Inventory Tracking
    * Billing and Payment Processing
    * Menu Management
    * Order Management

**2. Guest Menu Progressive Web App (PWA - Next.js on Vercel):**

* Accessible to guests via QR codes located at each table.
* URL structure: `https://your-resort.com/menu/{tableId}` (e.g., `https://your-resort.com/menu/T12`).
* Features:
    * Displays a live menu with real-time stock availability.
    * Allows guests to browse menu items.
    * Enables guests to add items to their cart.
    * Facilitates direct order submission to the staff.

## How the Guest PWA Works:

1.  **QR Codes at Tables:** Each table will have a unique QR code linking to a specific menu URL with a table identifier.
2.  **Next.js Dynamic Routing:** The PWA utilizes Next.js dynamic routes (`/menu/[tableId].tsx`) to display the menu based on the scanned table.
3.  **Real-Time Data:** The menu data (including stock counts) is pulled live from a real-time database (e.g., Firestore or Supabase Realtime).
4.  **Order Submission:** Guest orders are submitted through serverless functions (hosted on Vercel, e.g., `/api/placeOrder`) and written to an orders collection in the database.
5.  **Staff Notifications:** The staff mobile application listens for new orders in real-time, enabling prompt processing.

## Technologies Used:

* **Staff App:** React Native (Native Build)
* **Guest PWA:** Next.js, Vercel
* **Database:** (Specify your real-time database here, e.g., Firebase Firestore, Supabase Realtime)
* **Serverless Functions:** (Specify your platform if different from Vercel, e.g., Vercel Functions, AWS Lambda)

## Getting Started (for Developers):

*(You can add more detailed setup instructions here later as your project progresses, such as local development setup, environment variables, etc.)*

This application aims to enhance the operational efficiency of Chez Piera and provide a seamless and modern ordering experience for its guests.
