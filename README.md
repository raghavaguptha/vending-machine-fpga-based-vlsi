# vending-machine-fpga-based-vlsi



 

# 🥤 Vending Machine with Price Calculator (Verilog)

## 📌 Project Overview

This project is a **digital vending machine** designed and simulated using **Verilog**.
It accepts:

* The **quantity** of items selected
* The **price per item**
  and calculates the **total cost** in real time when the user presses the **select** button.

The design is fully synchronous with a clock signal and supports reset functionality.

---

## ⚙️ Features

* **Quantity & Price Input:** Adjustable via 4-bit and 8-bit inputs.
* **Instant Cost Calculation:** Multiplies `quantity × price_per_item`.
* **Dispense Signal:** Displays the number of items dispensed.
* **Total Cost Output:** Shows the total price for the current purchase.
* **Reset Function:** Clears all values.

---

## 🛠 Implementation Details

**Module:** `vending_machine_with_price.v`
**Testbench:** `tb_vending_machine_with_price.v`

### Working Principle

1. **Idle State:** All outputs are 0 until `select` is pressed.
2. **Transaction:** On `select`, the machine:

   * Dispenses the requested quantity
   * Calculates cost and total
3. **Reset / Deselect:** Values clear on reset or when `select` is released.

---

## 📊 Simulation Output

The design was simulated using **GTKWave**, and the waveform below shows:

* `quantity` & `price_per_item` changing over time
* Correct `cost` calculation in hexadecimal
* Dispense signal matching the selected quantity

Example:

| Time (ns) | Quantity | Price (hex) | Cost (hex) | Cost (dec) |
| --------- | -------- | ----------- | ---------- | ---------- |
| 37        | 2        | 0A          | 14         | 20         |
| 65        | 3        | 0A          | 1E         | 30         |
| 105       | 2        | 0F          | 1E         | 30         |

---



---

## 📂 File Structure

```
📦 vending-machine
 ┣ 📜 vending_machine_with_price.v   # Main Verilog module
 ┣ 📜 tb_vending_machine_with_price.v # Testbench
 ┗ 📷 waveform.png                    # Simulation result
```

---

## 🚀 How to Run

1. Open in **ModelSim**, **Vivado**, or **Icarus Verilog**.
2. Compile both `.v` files.
3. Run the simulation and open the waveform in GTKWave.

---

## 💡 Future Improvements

* Store last transaction even when `select` is released.
* Add multiple product selections.
* Implement payment verification before dispensing.

---

Do you want me to also make a **shorter, eye-catching version** so your GitHub visitors see the summary at a glance before the details? That would help make your project stand out more.


