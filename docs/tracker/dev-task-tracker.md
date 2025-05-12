---
id: dev-task-tracker
title: Dev Task Tracker
---
# ✅ Dev Task Tracker

## 🔧 Bugs to Fix

### 1. Streak Calculation Bug
- [ ] Fix streak logic:
  - Add +1 if any activity is logged today.
  - Subtract -1/reset if the only activity is undone today.
- [ ] On login:
  - If activity existed yesterday → keep streak.
  - If no activity yesterday → reset to 0.
- [ ] Bug: Streak sometimes resets to 0 on second login incorrectly.
- [ ] Bug: Streak value is wrongly updated in the database.
- [ ] Investigate where and when streak is recalculated (especially on login/state sync).

### 2. AsyncStorage Key on Login
- [ ] Fix: User data is saved under `'guest'` key after login.
- [ ] On login, AsyncStorage should use the correct `userId` key to save user data.

---

## 🛠️ Features to Implement

### 1. Pricing & Purchase Logic for Extra Activities
- [ ] Add `price` property to each item in `extraActivities` array.
- [ ] Add special “Add Custom Activity” item with a coin price.
- [ ] Logic:
  - If item is purchased → hide price, allow selection/removal.
  - If not purchased → show price and disable selection.

### 2. Custom Activities Flow
- [x] Modal UI for custom activity (icon + name) already implemented.
- [ ] Trigger modal after purchasing “Add Custom Activity”.
- [ ] Append custom activity to `extraActivities` after confirmation.
- [ ] Allow user to freely add/remove purchased custom activities.
- [ ] “Add Custom Activity” option should always be available for more purchases.

### 3. Font & Splash Screen Customization
- [ ] Replace app font with new one.
- [ ] Update splash screen with main logo.

---

## 🧪 Developer Tools

### 1. Add Coins in Dev Mode
- [x] Dev mode UI is implemented.
- [ ] Add a function to manually add coins to the current user (e.g., +10, +50, +100).