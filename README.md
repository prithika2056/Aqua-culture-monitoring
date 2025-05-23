# Aqua-culture-monitoring
# Arduino Water Quality Monitoring Simulation

This Arduino sketch simulates a **Water Quality Monitoring System** using potentiometers to mimic analog sensors. It's designed for prototyping and educational purposes, giving users a foundation to build upon with real sensors.

## 🧪 Simulated Parameters

The following water quality parameters are simulated using potentiometers:
- **pH Level** (Analog Pin A0)
- **Turbidity** (Analog Pin A1)
- **Dissolved Oxygen (DO)** (Analog Pin A2)
- **Ammonia (NH₃) Concentration** (Analog Pin A5)
- **Water Level** (Analog Pin A4 - simulating an ultrasonic sensor)

## 🚦 Thresholds and Alerts

| Parameter            | Thresholds                              | Description                                      |
|---------------------|------------------------------------------|--------------------------------------------------|
| pH Voltage           | 1.8V to 3.0V                             | Outside this range triggers acidic/alkaline alert |
| Turbidity            | > 500                                   | Indicates water is not clean                     |
| Dissolved Oxygen     | < 5% or > 15%                           | Unsafe for aquatic life                          |
| Ammonia Concentration| > 50% (High), < 5% (Low)               | High values are dangerous                        |
| Water Level          | < 10cm (Low), 10–30cm (Normal), >30cm (Full) | Based on simulated distance                     |

## 🛠️ How It Works

- Analog sensors (or potentiometers) provide simulated readings.
- Each reading is converted to a meaningful unit (e.g., % for DO and NH₃).
- Conditions are evaluated based on predefined thresholds.
- Results are printed to the Serial Monitor for debugging and analysis.

## 💻 Setup Instructions

1. Connect 5 potentiometers to analog pins A0, A1, A2, A4, and A5.
2. Upload the provided Arduino sketch to your board.
3. Open the Serial Monitor (9600 baud) to view the simulation in action.
4. Turn the potentiometers to simulate different environmental conditions.

## 🔧 Hardware Requirements

- Arduino Uno (or compatible board)
- 5x Potentiometers
- Jumper wires
- Breadboard

## 📦 Future Improvements

- Replace potentiometers with real sensors:
  - pH sensor
  - Turbidity sensor
  - Dissolved Oxygen sensor
  - Ammonia sensor
  - Ultrasonic distance sensor
- Add LCD or OLED display
- Add IoT features (ESP8266/ESP32 + WiFi + Cloud)
