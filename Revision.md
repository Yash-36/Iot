# Internet of Things (IoT) - Detailed Exam Preparation Notes

---

## **Unit 1: Introduction to IoT**

### Definition
- **Internet of Things (IoT)**: A dynamic network of interconnected physical objects embedded with sensors, actuators, software, and connectivity enabling them to collect and exchange data.
- Objective: Improve decision-making, efficiency, automation, and user experience.

### Key Characteristics of IoT
1. **Intelligence**: Devices generate meaningful insights from data.
2. **Identity**: Unique identifiers (UIDs) for each device.
3. **Scalability**: Supports large networks (millions of devices).
   - Horizontal scaling: Adding more devices.
   - Vertical scaling: Increasing processing/storage capacity.
4. **Self-Adaptation**: Devices adjust to environmental changes (e.g., smart irrigation).
5. **Security**: Protects data, devices, and communication from cyber threats.
6. **Architecture Interoperability**: Hybrid and flexible to integrate multi-vendor systems.

### Components of IoT
1. **Things/Devices**:
   - **Sensors**: Detect physical parameters (e.g., temperature, humidity).
   - **Actuators**: Perform actions based on processed data (e.g., motors).
2. **IoT Gateway**:
   - Interface between devices and cloud.
   - Handles protocol translation, security filtering.
3. **Cloud Platform**:
   - Stores, processes, and analyzes collected data.
   - Offers remote access and insights.
4. **Connectivity**:
   - Communication channels (Wi-Fi, Bluetooth, Zigbee, LoRaWAN).
5. **Analytics**:
   - Converts raw data into actionable insights using algorithms.
6. **User Interface (UI)**:
   - Dashboards, apps, and alerts for user interaction.

### IoT Architecture Stack (7 Layers)
1. **Physical/Sensor Layer**:
   - Sensors and actuators.
   - Data sensing and action execution.
2. **Control Action Layer**:
   - Microcontrollers (e.g., Arduino, Raspberry Pi).
   - Data acquisition and processing.
3. **Hardware Interface Layer**:
   - Interfacing standards like I2C, SPI, RS232.
4. **RF Communication Layer**:
   - Protocols: Wi-Fi, Bluetooth, ZigBee, LoRa.
   - EM wave-based data transmission.
5. **Session/Message Layer**:
   - Protocols: MQTT, CoAP.
   - Manages session control and message exchange.
6. **User Experience Layer**:
   - UI/UX design, visualization tools.
7. **Application Layer**:
   - Smart homes, smart cities, healthcare, etc.

---

## **Unit 2: IoT Physical Devices and Endpoints**

### IoT vs M2M
- **M2M**:
  - Machine-to-Machine, point-to-point communication.
  - No internet needed, limited scope.
- **IoT**:
  - Includes cloud computing, analytics, mobile access.

### Software Defined Network (SDN)
- Separates control plane from data plane.
- **Control Plane**: Routing, decision-making.
- **Data Plane**: Packet forwarding.

### Arduino UNO
- **Microcontroller**: ATmega328P
- **IDE**: Arduino Software (Processing-based).
- **Power Supply**: USB or 9V DC.
- **Digital I/O Pins**: 14 (6 PWM)
- **Analog Pins**: 6 (10-bit ADC)
- **USB-TTL Chip**: ATmega16U2
- **Onboard Components**:
  - LEDs (Power, Tx, Rx, Pin 13)
  - Reset button, voltage regulator, crystal oscillator
- **Arduino Shields**: Extend functionality (Wi-Fi, Ethernet, etc.)

---

## **Unit 3: Sensors & Actuators with Microcontrollers**

### Sensors
- **Function**: Detects physical/environmental changes and converts them to electrical signals.
- **Types**:
  - Analog: Variable output voltage (e.g., LDR, Gas sensor).
  - Digital: Binary output (e.g., Obstacle sensor).

### Examples
1. **LDR Sensor**:
   - Detects light intensity.
   - Used in voltage divider configuration.
2. **MQ Series (Gas Sensors)**:
   - Detects gas presence.
   - MQ-2 for smoke/LPG, MQ-7 for CO, MQ-135 for air quality.
3. **Obstacle Sensor**:
   - IR based, detects object presence.
   - Digital output (0/1).
4. **HC-SR04 Ultrasonic Sensor**:
   - Measures distance.
   - Uses Trigger and Echo pins.
   - Distance = (Time x Speed of Sound)/2
5. **Heartbeat Sensor**:
   - Detects pulse via light transmission.
   - Analog output.

### Interfacing with Arduino
- **Commands**:
  - `analogRead(pin)`, `digitalRead(pin)`
  - `Serial.begin()`, `Serial.print()`, `delay()`

---

## **Unit 4: IoT Protocols**

### Serial Communication
- **Serial**: Bit-by-bit transmission (UART, SPI, I2C).
- **Parallel**: Multi-bit transmission (faster, short-range).

### UART (Universal Asynchronous Receiver Transmitter)
- No clock signal.
- Frame: Start bit - Data bits - Parity bit - Stop bit
- **Baud Rate**: Speed of communication (e.g., 9600 bps).
- **Flow Control**:
  - Hardware: RTS/CTS
  - Software: XON/XOFF

### Arduino Serial Functions
- `Serial.begin(baudRate)`
- `Serial.print()`, `Serial.println()`
- `Serial.read()`, `Serial.available()`
- `Serial.write(data)`

### SPI (Serial Peripheral Interface)
- **Synchronous**: Master-Slave architecture.
- Pins:
  - MOSI: Master → Slave
  - MISO: Slave → Master
  - SCLK: Clock by master
  - SS: Slave select

### I2C (Inter-Integrated Circuit)
- Two-wire: SDA (data), SCL (clock)
- Master-Slave, address-based

### Software Serial (Arduino)
- Create additional UART using any digital pins.
- Limited speed and only one active receiver at a time.

---

## **Unit 5: Domain Specific Applications of IoT**

### 1. Healthcare
- **Use Cases**: Remote monitoring, health tracking, alerting caregivers.
- **Components**: Heartbeat sensor, glucose sensor, NodeMCU, Fog computer, Cloud.
- **Architecture**:
  - Sensors → Controller → Fog → Cloud → Caregiver

### 2. Retail
- **Use Cases**: Inventory management, customer behavior, safety.
- **Components**: RFID, Beacons, Fire/Gas sensors, Arduino/ESP32.
- **Applications**:
  - Automated billing, customer alerts, environmental monitoring.

### 3. Driver Assistance
- **Use Cases**: Drowsiness detection, accident prevention.
- **Tech**: Image processing, Machine Learning, EAR detection.
- **Components**: Camera, Ultrasonic, OBD, Raspberry Pi, Cloud.
- **Actions**: Alert generation, vehicle control interventions.

### Common Architecture for IoT Apps
1. Sensor Nodes
2. Controller (local logic)
3. Fog Node (filter & alert)
4. Cloud Server (analytics & storage)
5. Actuators or end-users (response/action)

---

### End of Notes
