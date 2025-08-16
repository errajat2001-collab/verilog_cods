# 4-Bit Adder (Verilog - Vivado Project)

## 📘 Overview

This project implements a **4-bit binary adder in Verilog HDL**, built and simulated using **Xilinx Vivado**. The design takes two 4-bit inputs and produces a 4-bit sum with a carry-out. A testbench is included for functional verification.

---

## ⚡ Features

* Implemented in **Verilog HDL**
* Full Vivado project provided (`.xpr` file)
* Includes **testbench and waveform configuration**
* Ready for **simulation and synthesis** in Vivado
* Project files are provided in a **compressed folder (`4_bit_adder.zip`)**

---

## 🛠️ Implementation

The design uses **four 1-bit full adders** connected in series:

* **FA0** → Adds `A0`, `B0`, `Cin`
* **FA1** → Adds `A1`, `B1` + carry from FA0
* **FA2** → Adds `A2`, `B2` + carry from FA1
* **FA3** → Adds `A3`, `B3` + carry from FA2

The final carry-out (`Cout`) indicates overflow.

---

## 🖥️ How to Run

1. **Download and extract** the project folder:

   ```bash
   unzip 4_bit_adder.zip
   cd 4_bit_adder
   ```

2. **Open in Vivado**

   * Launch Vivado
   * Open the project: `File → Open Project → 4_bit_adder.xpr`

3. **Run Simulation**

   * In the Flow Navigator, select **Run Simulation → Run Behavioral Simulation**
   * The waveform (`adder4bit_tb_behav.wcfg`) will show input/output signals

4. **Run Synthesis & Implementation (Optional)**

   * Use **Run Synthesis** and **Generate Bitstream** if targeting FPGA

---

## 🔍 Example

Input:

* A = `1011` (11 in decimal)
* B = `0110` (6 in decimal)

Output:

* Sum = `0001` (1 in decimal)
* Cout = `1`

➡ Result = `1 0001` (17 in decimal)

---

## 📂 Project Structure

```
4_bit_adder/
│── 4_bit_adder.xpr             # Vivado project file
│── adder4bit_tb_behav.wcfg     # Testbench waveform config
│── 4_bit_adder.cache/          # Vivado cache files
│── 4_bit_adder.hw/             # Hardware files
│── 4_bit_adder.ip_user_files/  # IP-related files
│── 4_bit_adder.runs/           # Synthesis & implementation runs
```

---

## 📖 References

* *Digital Design* by M. Morris Mano
* *Fundamentals of Logic Design* by Charles H. Roth
* [Xilinx Vivado Documentation](https://docs.xilinx.com/)

---
