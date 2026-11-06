# AgriConnect — React + Vite

A React implementation of the AgriConnect marketplace using Vite.

## Main modules

### 1. Admin module
- Admin login
- View registered users
- View and remove product listings
- View demo orders
- Admin dashboard with summary counts

### 2. User module
Users register as one of two user types:
- **Farmer:** add produce listings and view orders for their produce.
- **Buyer:** browse and search products, filter by category, place demo orders and view order history.

## Run locally

1. Install Node.js (LTS).
2. Extract this folder and open it in VS Code.
3. Open a terminal in this folder and run:

```bash
npm install
npm run dev
```

4. Open the local URL printed by Vite (usually http://localhost:5173).

## Run with VS Code Go Live

Live Server cannot compile React JSX by itself. To use the **Go Live** button:

1. Run `npm install` once.
2. Run `npm run build` whenever you want to refresh the app.
3. Open `index.html` in VS Code and click **Go Live**. The workspace Live Server setting serves the generated `dist` folder.

Go Live serves the last production build, so it does not automatically rebuild when source files change. Use `npm run dev` for live development with automatic updates.

## Production build

```bash
npm run build
npm run preview
```

## Deploy to GitHub Pages

The GitHub Actions workflow builds and deploys this app to Pages whenever changes are pushed to `main`. In the repository settings, open **Pages** and set the build and deployment source to **GitHub Actions**. The project site will be available at:

`https://vajrapunagarushyendhra.github.io/Project/`

## Demo admin login
- Email: `admin@agriconnect.demo`
- Password: `Admin123`

On the login page, select **Admin** to use the demo admin account or **User** to sign in to a registered Farmer or Buyer account. Create User accounts from the sign-up page.

## Project structure
- `src/App.jsx` — React state, navigation, forms, Admin/User modules, marketplace and dashboard logic.
- `src/style.css` — responsive stylesheet.
- `src/main.jsx` — React entry point.
- `index.html` — Vite HTML entry point.

## Local Storage and limitations
Accounts, products, orders and the login session are stored in browser Local Storage for demonstration. Existing Farmer/Buyer accounts created by the earlier version are migrated to the User role while retaining their Farmer/Buyer user type. This is not secure authentication and data is not shared between browsers or devices. Do not enter real passwords or sensitive information. A production app needs a backend, secure authentication/authorization and a database.
