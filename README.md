# 🧠 6T SRAM Cell Design – Schematic & Layout (Electric VLSI Free Tool)

This project demonstrates the **design of a 6-Transistor (6T) SRAM memory cell** using the **Electric VLSI Design System**. It includes only the **schematic and layout**—simulation and waveform outputs are not included in this repository.

---

## 📌 Project Overview

A **6T SRAM cell** is the fundamental memory element used in static RAM chips. It consists of:

- **2 cross-coupled CMOS inverters** (4 transistors total: 2 NMOS, 2 PMOS)
- **2 NMOS access transistors**, controlled by a wordline
- **2 complementary bitlines** for read/write operations

This project focuses on:
- Creating a **schematic** that properly represents the internal structure of the 6T cell.
- Developing a **clean layout** with proper DRC-clean rules using Electric VLSI.
- Ensuring correct connectivity and transistor sizing for stable operation.

---

## 🧰 Tools Used

| Tool              | Purpose                    |
|------------------|----------------------------|
| Electric VLSI     | Schematic & Layout Editing |
| Ubuntu 20.04+     | Development Environment    |

> 🔗 [Electric VLSI GitHub - Download and Installation Guide](https://github.com/DuttPanchal04/electric-vlsi-design-free-tool-installation-guide)

---

## 📂 Folder Structure
```
SRAM_CELL/
├── schematic (.png)
├── layout (.png)
└── project library ( .jelib )
```

---

## 🧑‍💻 Design Details

### ➤ Schematic

- **Tool**: Electric VLSI
- **Transistor Count**: 6 (2 PMOS, 4 NMOS)
- **Design Notes**:
  - Access transistors are controlled via the **Wordline**.
  - Data read/write via **Bitline** and **Bitline_Bar**.
  - Internal state stored between nodes **Q** and **Q_Bar**.

![6T SRAM CELL CMOS CIRCUIT DESIGN](https://github.com/user-attachments/assets/93c49204-61b2-41e0-82ed-e3657c9f7cf5)

### ➤ Layout

- Created in **Electric VLSI** using custom standard cells.
- Connections match schematic 1:1 (DRC clean).
- DRC/LVS/ERC passed successfully.

![6T SRAM CELL CMOS LAYOUT DESIGN](https://github.com/user-attachments/assets/bf638644-23bc-46ea-8e21-eb9626524c7f)

---

## 📏 Transistor Sizing

| Transistor Type | Width (W) | Notes                            |
|-----------------|-----------|----------------------------------|
| PMOS            | 5 λ       | Sufficient for pull-up strength |
| NMOS            | 10 λ      | Stronger pull-down path         |

> λ = Lambda unit (technology dependent)

These values ensure **cell stability** during read and write operations for a basic technology node.

---

## 📝 How to View the Project

1. **Install Electric VLSI** from the GitHub repo or a Linux package manager.
2. Open Electric VLSI.
3. Use `File → Open Library → project.jelib`  .
4. Navigate through the hierarchy and explore both schematic and layout designs.

---

## 🛠️ Features Implemented

- ✅ 6T SRAM Schematic with labeled signals: `Q`, `Q_BAR`, `BITLINE`, `BITLINE_BAR`, `WORDLINE`
- ✅ CMOS Inverter pairs + access transistors
- ✅ DRC-clean layout (manual routing)
- ✅ LVS ( Layout vs Schematic ) passed successfully. 
- ✅ ERC passed.
- ✅ Technology-independent design (lambda-based)

## 📣 Author

**Dutt Panchal**  
Electronics & Communication Engineering Student
💼 Final Year | VLSI Design Enthusiast | Electric VLSI + Open-Source Tools  

- 📧 Email: dattpanchal2904@gmail.com
- 🔗 [LinkedIn](https://www.linkedin.com/in/dattpanchal04/) 
- 🌐 [GitHub](https://github.com/DuttPanchal04)

---

## 📌 Future Improvements

- Add **waveform simulation** (read/write testbench)
- Perform **LVS** and **extraction**
- Explore **array-level** integration for multi-bit SRAM
- Port design to **Sky130 or other PDKs** for fabrication-ready flow

---

## 📎 License

This project is open-source and free to use for educational and academic purposes.  
Feel free to fork, modify, and contribute!

---

⭐️ *If you found this helpful or interesting, drop a star on GitHub and connect on LinkedIn!*
