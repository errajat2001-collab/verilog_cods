# 4-Bit Adder (Verilog)

## 📘 Overview

This project implements a **4-bit binary adder in Verilog HDL**. The circuit adds two 4-bit binary numbers and outputs their sum along with a carry-out bit. It demonstrates the use of **structural modeling** with full adders and is a basic building block for larger arithmetic circuits.

---

## ⚡ Features

* Written in **Verilog HDL**
* Adds two 4-bit binary inputs (`A[3:0]`, `B[3:0]`)
* Produces a **4-bit sum (`S[3:0]`)** and a **carry-out (`Cout`)**
* Designed for simulation in tools like **ModelSim / Vivado / Quartus**
* Source code is provided in a **compressed folder (`src.zip`)**

---

## 🛠️ Implementation

The adder is built using **four full adders** connected in series:

1. **FA0** → Adds `A0`, `B0`, and `Cin`
2. **FA1** → Adds `A1`, `B1`, and carry from FA0
3. **FA2** → Adds `A2`, `B2`, and carry from FA1
4. **FA3** → Adds `A3`, `B3`, and carry from FA2

The final carry-out (`Cout`) indicates overflow.

---

## 🖥️ How to Run

1. **Download and extract the project**

   * Locate the compressed source folder: `src.zip`
   * Extract it to your working directory

2. **Open in a Verilog simulator**

   * Import the `.v` files from the extracted folder into your preferred simulator (ModelSim, Vivado, Quartus, etc.)

3. **Compile and run the testbench**

   * Compile `full_adder.v`, `adder4bit.v`, and `testbench.v` (if provided)
   * Run simulation to verify the output

4. **Check results**

   * The simulation waveform will display inputs (`A`, `B`) and outputs (`S`, `Cout`)

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
4-bit-adder/
│── src.zip       # Compressed folder containing Verilog source files
│── README.md     # Project documentation
```

Inside `src.zip`:

```
src/
│── full_adder.v      # 1-bit full adder module
│── adder4bit.v       # 4-bit adder module (structural)
│── testbench.v       # Testbench for simulation
```

---

## 📖 References

* *Digital Design* by M. Morris Mano
* *Fundamentals of Logic Design* by Charles H. Roth
* [Verilog Full Adder Example](https://en.wikipedia.org/wiki/Adder_%28electronics%29)

---
