![fulo](https://github.com/user-attachments/assets/da884465-6bb6-4b7d-b9fe-5036ac96e095)
# Fulo Food App Documentation

## 1. Project Overview

### Title
Fulo: The Fullstack Food App

### Description
Fulo is a full-featured food application that allows users to list, search, and inquire about food items available at various restaurants. It also includes functionality for placing orders directly through the app. The application is developed using Flutter for the frontend, GetX for state management, and Supabase as the backend database solution.

---

## 2. Features

### Core Features
1. **Food Listing:**
   - Restaurants can list their food items with details like name, description, price, and availability.
   - Includes support for adding images of food items.

2. **Search and Filter:**
   - Users can search for food items by name, cuisine, or restaurant.
   - Advanced filters for price range, availability, and ratings.

3. **Inquiries:**
   - Users can inquire about specific dishes or request customizations.
   - Communication via in-app messaging or email integration.

4. **Food Ordering:**
   - Users can add items to a cart and place orders.
   - Includes order tracking and status updates.

5. **User Authentication:**
   - Secure user registration and login via Supabase authentication.
   - Social login options (Google, Facebook, etc.).

6. **Restaurant Management Panel:**
   - Restaurants can manage their menus, update availability, and view orders.

7. **Notifications:**
   - Push notifications for order updates, special deals, and promotions.

---

## 3. Technologies Used

### Frontend
- **Flutter**: Framework for building the app’s UI and interactions.
- **GetX**: For state management, routing, and dependency injection.

### Backend
- **Supabase**: Used for database management, authentication, and real-time updates.

### Packages Used
#### Flutter Packages:
- **get:** For state management.
- **flutter_secure_storage:** For storing sensitive data securely.
- **http:** For API calls.
- **cached_network_image:** For optimized image loading.
- **firebase_messaging:** For push notifications.
- **intl:** For formatting dates and currencies.

---

## 4. Installation and Setup

### Prerequisites
- Flutter SDK installed.
- A Supabase account with an active project.
- Android Studio or VS Code for development.

### Steps
1. **Clone the Repository:**
   ```bash
   git clone <repository-url>
   cd fulo-food-app
   ```

2. **Set Up Supabase:**
   - Create a new project in Supabase.
   - Set up authentication and database tables for users, restaurants, and orders.
   - Update the Supabase URL and API Key in the project.

3. **Install Dependencies:**
   ```bash
   flutter pub get
   ```

4. **Run the App:**
   ```bash
   flutter run
   ```

---

## 5. Database Structure

### Tables
1. **Users:**
   - `id` (Primary Key)
   - `name`
   - `email`
   - `password`
   - `role` (user/restaurant)

2. **Restaurants:**
   - `id` (Primary Key)
   - `name`
   - `location`
   - `contact_info`

3. **Food_Items:**
   - `id` (Primary Key)
   - `restaurant_id` (Foreign Key)
   - `name`
   - `description`
   - `price`
   - `availability`
   - `image_url`

4. **Orders:**
   - `id` (Primary Key)
   - `user_id` (Foreign Key)
   - `restaurant_id` (Foreign Key)
   - `order_details` (JSON)
   - `status` (pending/confirmed/completed)
   - `timestamp`

---

## 6. Usage

### User Workflow
1. Register or log in to the app.
2. Search for food items or browse restaurants.
3. Add desired items to the cart.
4. Place an order and track its status.
5. Receive notifications about order updates or promotions.

### Restaurant Workflow
1. Log in to the app using restaurant credentials.
2. Add or update food items and availability.
3. Manage incoming orders and update their status.

---

## 7. Challenges and Learnings

### Challenges
- Integrating real-time updates using Supabase.
- Designing an intuitive UI for both users and restaurants.
- Managing state effectively across complex user workflows.

### Learnings
- Gained expertise in Flutter and GetX for building scalable mobile applications.
- Improved understanding of Supabase for backend solutions.
- Learned to optimize API calls and handle real-time data efficiently.

---

## 8. Future Enhancements

1. **Enhanced Payment Integration:**
   - Add support for payment gateways (Stripe, PayPal, etc.).

2. **Review System:**
   - Allow users to leave reviews and ratings for restaurants and dishes.

3. **Delivery Tracking:**
   - Add GPS tracking for delivery personnel.

4. **Analytics Dashboard:**
   - Provide restaurants with insights into sales and customer behavior.

5. **Multi-language Support:**
   - Enable localization for a wider audience.

---

## 9. References
- [Flutter Documentation](https://flutter.dev/docs)
- [GetX Documentation](https://pub.dev/packages/get)
- [Supabase Documentation](https://supabase.com/docs)
- [Flutter Secure Storage](https://pub.dev/packages/flutter_secure_storage)

---

## 10. Conclusion
Fulo is an innovative food application that simplifies food discovery and ordering for users while providing restaurants with a platform to manage their offerings efficiently. With a robust tech stack and user-friendly design, Fulo is poised to enhance the food ordering experience for all stakeholders.

