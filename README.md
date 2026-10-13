# Credential Stuffing Attack Detection Website

This is a browser-based demo website for the project:
**Credential Stuffing Attack Detection Using Gradient Boosting Machine and Isolation Forest**

## Run in VS Code

1. Extract the ZIP file.
2. Open the `credential-stuffing-detection-website` folder in Visual Studio Code.
3. Open `index.html`.
4. Right-click inside the editor and select **Open with Live Server** (if you have the Live Server extension).
   - If you do not have Live Server, you can double-click `index.html` to open it in your browser.
5. Create an account on the sign-in screen, then sign in to use the dashboard.

## Website features

- Sign-in and account creation (stored in this browser)
- Dashboard with sample login statistics and charts
- Login analysis with search and filters
- Attack simulation
- ML prediction demo using login-traffic features
- Analytics and sample model metrics
- Alerts with demo IP block/unblock controls
- Project overview

## Important note

This version is a **front-end demonstration**. The prediction function uses a formula to imitate Gradient Boosting and Isolation Forest; it does not load a trained machine-learning model or block real IP addresses. The displayed analytics and confusion matrix are sample/demo values. Connect a Python backend and your trained models if you need real predictions.

The charts use Chart.js from a CDN, so an internet connection is needed for the charts to load.
