# Welcome to VERIGEN!

```
 ___      ___ _______   ________  ___  ________  _______   ________      
|\  \    /  /|\  ___ \ |\   __  \|\  \|\   ____\|\  ___ \ |\   ___  \    
\ \  \  /  / | \   __/|\ \  \|\  \ \  \ \  \___|\ \   __/|\ \  \\ \  \   
 \ \  \/  / / \ \  \_|/_\ \   _  _\ \  \ \  \  __\ \  \_|/_\ \  \\ \  \  
  \ \    / /   \ \  \_|\ \ \  \\  \\ \  \ \  \|\  \ \  \_|\ \ \  \\ \  \ 
   \ \__/ /     \ \_______\ \__\\ _\\ \__\ \_______\ \_______\ \__\\ \__\
    \|__|/       \|_______|\|__|\|__|\|__|\|_______|\|_______|\|__| \|__|
```

### Author:
**Albert Cheung (Lee-Khai Cheung)**
**Email: albert.chg9@gmail.com**
---

## Installation and Configuration

### Prerequisites:
- **Linux** (Fedora 41 best, or any Unix-like OS)
- **Verigen tools**, include
  - `iverilog`
  - `yosys`
  - `netlistsvg`
  - `vvp`
- *In fact, these are not necessary. If you don't, you can simply run it in the Verigen shell environment. Verigen has offered you these tools.*

### Steps to Install:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/verigen.git
   cd verigen
   ```

2. **Build and configure:**
   Make sure your environment is properly set up to run Verigen.
   Inside the `verigen` directory, run:
   ```bash
   chmod +x build
   ./build
   ```

   After installation, you should be able to run `verigen` directly from anywhere in the terminal.

---

## Simple Instructions

### Running Verigen:
1. **Enter the interactive Verigen shell:**
   ```bash
   verigen
   ```
   This will enter the Verigen interactive shell. From here, you can enter Verigen commands directly.

2. **Run Verilog simulation:**
   ```bash
   verigen testbench.v dut.v
   ```
   This will run a simulation using the `iverilog` compiler and `vvp` simulation tool. It will generate output and remove intermediate files (`simv`).

3. **Generate netlist and SVG:**
   ```bash
   verigen -a dut.v
   ```
   This command generates a JSON netlist and an SVG diagram for the given Verilog file.

4. **Generate only netlist (no SVG):**
   ```bash
   verigen -j dut.v
   ```
   This command generates only the JSON netlist without the SVG diagram.

5. **Generate netlist and SVG, then delete SVG:**
   ```bash
   verigen -s dut.v
   ```
   This command generates both the JSON netlist and the SVG diagram, then deletes the SVG file after generation.

6. **Check Verigen version:**
   ```bash
   verigen --version
   ```
   Displays the current version of Verigen.

7. **Get help:**
   Inside the interactive shell, type:
   ```bash
   .help
   ```
   This will show you a list of all available commands and options in Verigen.

---

## License

This software is released under the [MIT License](LICENSE).
```

---