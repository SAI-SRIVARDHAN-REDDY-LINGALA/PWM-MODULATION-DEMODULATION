# PWM-MODULATION-DEMODULATION
PULSE WIDTH MODULATION,DEMODUALTION


# 📜 **README: PWM Modulation & Demodulation using LTspice** 🚀  

## 🎯 **Project Overview**  
This project demonstrates **Pulse Width Modulation (PWM) and Demodulation** using **LTspice**. PWM is widely used in **signal processing, motor control, communication systems, and power electronics**. The goal is to design a **PWM generator** and a **demodulator** to recover the original message signal using **op-amps and passive components**.  

## 🛠 **Objectives**  
✔️ **Generate** a PWM signal by comparing a 1 kHz message signal with a 10 kHz carrier signal.  
✔️ **Demodulate** the PWM signal using a **second-order active low-pass filter** to recover the original message.  
✔️ **Bonus**: Extract the **carrier signal** from the PWM waveform using a **4th-order band-pass filter**.  

## 📌 **Project Details**  

### ⚡ **PWM Generation**  
🔹 **Message Signal**: 1 kHz sine wave, 5V amplitude.  
🔹 **Carrier Signal**: 10 kHz sine wave, 5V amplitude.  
🔹 **Comparator Circuit**: Uses **Universal Op-Amp (U4 in LTspice)** for signal comparison.  
🔹 **Expected Output**: Square wave PWM signal where pulse width varies based on message signal amplitude.  

🔹 **Key Learnings from Op-Amps**:  
- **High Gain-Bandwidth Product (GBW)** ensures sharp transitions.  
- **Higher Slew Rate** helps in rapid switching.  
- **Proper Power Supply** is critical for full output transitions.  

### 🎛 **PWM Demodulation**  
🔹 **Method**: Uses a **Sallen-Key Second-Order Active Low-Pass Filter** to recover the message signal.  
🔹 **Cutoff Frequency**: ~1.5 kHz (close to message frequency).  
🔹 **Components**:  
   - Resistors: 12kΩ, 1kΩ  
   - Capacitors: 100nF  
   - Op-Amp Power: ±10V  
🔹 **Expected Output**: A smooth sine wave (with slight phase shift).  

### 🎵 **Bonus: Carrier Signal Extraction**  
🔹 **Uses a 4th-Order Butterworth Band-Pass Filter**  
🔹 **Advantages over High-Pass Filter**:  
   - **Better selectivity**: Passes only carrier range (5 kHz – 15 kHz).  
   - **Suppresses unwanted harmonics** for cleaner signal extraction.  
   - **Minimal Phase Distortion**: Ensures accurate waveform recovery.  

## 🚀 **How to Run the Simulation**  
1️⃣ **Download and Install LTspice** from [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html).  
2️⃣ **Open the LTspice project files**.  
3️⃣ **Run the simulation** and observe:  
   - **PWM waveform**  
   - **Demodulated message signal**  
   - **Extracted carrier signal** (bonus)  
4️⃣ **Compare the original and recovered signals** using the waveform viewer.  

## 📂 **Project Files**  
📜 `PWM.asc` → LTspice schematic for PWM signal generation.  
📜SCREENSHOTS - PLOT OF RESULTS 
📜 `README.md` → This documentation.  

## 🔬 **Results & Observations**  
✔️ **PWM generation successfully encodes the message signal**.  
✔️ **Demodulation retrieves the original sine wave with minimal distortion**.  
✔️ **Carrier extraction using BPF provides a clean extracted waveform**.  

## 🎯 **Future Improvements**  
✅ Experiment with **higher-order filters** for even smoother signal recovery.  
✅ Implement this system **on hardware using op-amp ICs** for real-world testing.  
✅ Optimize component values for **better performance in noisy environments**.  

## 🎓 **References**  
📖 **LTspice Tutorials**: [LTspice Official Guide](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)  
📖 **Signal Processing with Op-Amps**: [Op-Amp Basics](https://www.ti.com/lit/an/sboa092a/sboa092a.pdf)  

---
🛠️ **Designed & Simulated by:** *Sai Srivardhan Lingala* 🚀  
📌 **Project for:** IIT Kharagpur EECE 🏫  
📅 **Year:** 2025  
