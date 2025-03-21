# Kalman Filter Implementation in Python

## 📌 Introduction
This project demonstrates a **Kalman Filter** for estimating the position of an object moving in one dimension with noisy measurements. The Kalman Filter is an optimal recursive algorithm used for tracking and prediction in control systems, robotics, and sensor fusion.

## 🚀 Features
- Predicts the object's position using a **state-space model**.
- Updates the prediction using noisy **sensor measurements**.
- Implements the **Kalman equations** for prediction and update steps.
- **Visualizes results** using a bar graph.

## 🏗️ Kalman Filter Equations
### **1️⃣ Prediction Step**
- Predict the next state:
  
  \[ \hat{x}_k^- = F \hat{x}_{k-1} + B u_k \]
  
- Predict the next covariance:
  
  \[ P_k^- = F P_{k-1} F^T + Q \]
  
### **2️⃣ Update (Correction) Step**
- Compute the **Kalman Gain**:
  
  \[ K_k = P_k^- H^T (H P_k^- H^T + R)^{-1} \]
  
- Update the state estimate:
  
  \[ \hat{x}_k = \hat{x}_k^- + K_k (z_k - H \hat{x}_k^-) \]
  
- Update the error covariance:
  
  \[ P_k = (I - K_k H) P_k^- \]

## 🛠️ Installation
To run this project, install the required libraries:
```bash
pip install numpy matplotlib
```

## 📜 Usage
Run the `main.py` script to see the Kalman Filter in action.
```bash
python main.py
```

## 📊 Visualization
The output includes a **bar graph** comparing:
- **Red bars** → Noisy sensor measurements
- **Blue bars** → Kalman Filter estimated position

## 📝 Example Output
```
Predicted state:
 [[0.5]
 [1.0]]
Updated state:
 [[1.1]
 [1.2]]
```

## 📚 Applications
- **Object Tracking** (drones, robotics, self-driving cars)
- **Sensor Fusion** (combining data from multiple sensors)
- **Financial Forecasting** (predicting stock prices)
- **Navigation Systems** (GPS-based positioning)

## 📌 Contributing
Feel free to fork this repo and improve the implementation. If you have suggestions or find issues, create a pull request! 🚀

## 📜 License
This project is licensed under the MIT License.
