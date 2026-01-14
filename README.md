# IoT Wireless Door Alarm System (Micro:bit)

## 📝 Project Description
This project features a **wireless security alarm system** designed to monitor door activity in real-time. Built using two **BBC micro:bit v1** boards, the system leverages radio frequency communication and integrated sensors to detect movement and prevent unauthorized entries.

The system consists of two main modules:
1.  **Transmitter (Door Sensor):** Mounted on the door, it utilizes the onboard accelerometer to detect sudden shifts in position. Upon detecting movement, it broadcasts an alert signal via radio.
2.  **Receiver (User Unit):** Located remotely, it receives alert notifications and provides visual feedback to the user, indicating whether the door has been opened or secured.

## ⚙️ Technical Logic
* **Communication:** Low-power digital radio communication on `radio.setGroup(17)`.
* **Event Handling:** * **Motion Event:** Accelerometer detects a "shake" or "tilt" → sends "open" signal → displays **"X"** on both units.
    * **User Reset:** Pressing **Button A** on the receiver → sends "closed" signal → displays a **"Checkmark" (Tick)** on both units to re-arm the system.

## 🛠️ Hardware Requirements
* **2x BBC micro:bit v1** – [Micro:bit Overview](https://microbit.org/get-started/features/overview/)
* **2x AAA Battery Packs** with batteries
* **Double-sided adhesive tape** (for mounting the transmitter unit)

### Hardware Components:
![Micro:bit Board](https://github.com/user-attachments/assets/61eb9445-9036-4901-841f-49b7228bf66d)

![Complete Kit](https://github.com/user-attachments/assets/74337582-3ccb-4b30-bf79-4d761f04ee2f)

## 💻 Software & Environment
* **Microsoft MakeCode:** Online Block/JavaScript Editor.
* **Radio Protocol:** Integrated micro:bit radio frequency module for low-latency communication.

## 🚀 Setup and Build
1.  Open [MakeCode for micro:bit](https://makecode.microbit.org/).
2.  Import the source code files:
    * `transmitter.py` (for the door-mounted unit).
    * `receiver.py` (for the remote user unit).
3.  Flash the generated `.hex` files onto the respective micro:bit boards via USB.
4.  Mount the **Transmitter** to the door frame/surface using double-sided adhesive tape.
5.  Power both units; they will automatically sync on the pre-defined radio group.

## 🚦 Operation
1.  **Trigger:** When the door is opened or moved, the Transmitter detects the motion.
2.  **Alert:** An **"X"** icon appears instantly on both the sensor and the remote user unit.
3.  **Reset:** The user acknowledges the alert by pressing **Button A** on the Receiver.
4.  **Armed State:** Both boards display a **"Tick"** icon, and the system returns to its monitoring state.
