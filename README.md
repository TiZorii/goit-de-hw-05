# "Apache Kafka"

Are you ready? Let’s get started! 🎢

Today, I’ll focus on the practical use of Apache Kafka through the Python API, honing my skills in creating topics, writing data to a topic, and reading from it.

---

### Scenario:

Imagine I’m working at a company developing monitoring systems for the Internet of Things (IoT). The main task of the system is to collect data from various sensors installed in multiple buildings and analyze this data in real-time to track parameters such as temperature and humidity.

For this, Apache Kafka is used as a messaging platform, enabling efficient transmission and processing of large volumes of data.

My task is to implement several components of this system using Python and Apache Kafka, following the provided instructions.

Let this assignment broaden my perspective on the world of streaming data! 🧠

---

### Step-by-Step Instructions

#### **1. Creating Topics in Kafka**

I’ll create three topics in Kafka:
- To avoid duplication, I’ll add my name or another identifier to the topic names.
  - **`building_sensors`** — for storing data from all sensors.
  - **`temperature_alerts`** — for storing alerts about exceeding acceptable temperature levels.
  - **`humidity_alerts`** — for storing alerts about humidity levels outside the acceptable range.

---

#### **2. Sending Data to Topics**

I’ll write a Python script that simulates a sensor and periodically sends randomly generated data (temperature and humidity) to the **`building_sensors`** topic.
- The data must include the **sensor ID**, **timestamp**, and corresponding measurements.
- One script run should correspond to only one sensor. To simulate multiple sensors, I’ll run the script several times.
- The **sensor ID** can be a random but constant number for one script run. Upon restarting, the sensor ID may change.
- **Temperature** will be a random value between **25 and 45°C**.
- **Humidity** will be a random value between **15 and 85%**.

---

#### **3. Processing Data**

I’ll write a Python script that subscribes to the **`building_sensors`** topic, reads messages, and processes the data:
- If the **temperature exceeds 40°C**, it generates an alert and sends it to the **`temperature_alerts`** topic.
- If the **humidity exceeds 80%** or drops below 20%, it generates an alert and sends it to the **`humidity_alerts`** topic.

Alerts must include the **sensor ID**, **measurement values**, **timestamp**, and a **message** about the threshold being exceeded.

---

#### **4. Final Data**

I’ll write a Python script that subscribes to the **`temperature_alerts`** and **`humidity_alerts`** topics, reads the alerts, and displays them on the screen.
