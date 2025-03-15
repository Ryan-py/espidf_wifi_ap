### 🚀 **ESP32-C6 Xiao: Wi-Fi AP with LED Indicator**  

This project sets up the **Seeed Studio XIAO ESP32-C6** as a Wi-Fi Access Point (AP) and blinks an LED to indicate activity.  

---

## 📌 **Features**  
✅ Creates a Wi-Fi AP named **"it_hurts_when_IP"** with password **"12345678"**  
✅ Logs when devices connect or disconnect  
✅ Blinks an LED on **GPIO 15**  

---

## 🔧 **Hardware Setup**  
- **XIAO ESP32-C6** board  
- **LED connected to GPIO 15** (or use onboard LED if available)  

---

## 🛠 **Installation**  
1️⃣ Install **ESP-IDF** (latest version recommended)  
2️⃣ Clone or copy the project files  
3️⃣ Compile and flash using:  
   ```sh
   idf.py build flash monitor
   ```  

---

## 📜 **Code Overview**  
### **1. Wi-Fi AP Initialization (`my_ap_init()`)**  
- Sets up ESP32-C6 in **AP mode**  
- Allows up to **10 connections**  
- Logs connection/disconnection events  

### **2. LED Indicator Task (`led_indicator()`)**  
- Blinks LED every **500ms**  

### **3. Event Handling (`wifi_event_handler()`)**  
- Logs MAC address of connected/disconnected devices  

---

## ⚡ **Example Log Output**  
```
I (1000) My_AP_cool: Wi-Fi AP started. SSID: it_hurts_when_IP
I (2000) Wi-Fi: Device connected: AA:BB:CC:DD:EE:FF, AID=1
I (5000) Wi-Fi: Device disconnected: AA:BB:CC:DD:EE:FF, AID=1
```

---

## 📝 **Customization**  
- Change **SSID & password** in `wifi_config_t`  
- Modify **LED blink rate** in `vTaskDelay()`  

Enjoy your **ESP32-C6 Wi-Fi AP project!** 🎉