# Verilog Environment Setup

This repository provides a step-by-step guide to setting up **Icarus Verilog** and **GTKWave** on Ubuntu/Linux systems. These tools are essential for simulating and debugging Verilog designs.

## 📌 Features
- Install **Icarus Verilog** (iverilog) for compiling Verilog code.
- Install **GTKWave** for waveform visualization.
- Verify the installation with a simple Verilog testbench.

## 🛠 Installation
Follow these steps to set up your environment:

### **1. Update Your System**
```sh
sudo apt update && sudo apt upgrade -y
```

### **2. Install Icarus Verilog (iverilog)**
```sh
sudo apt install iverilog -y
```
Verify the installation:
```sh
iverilog -V
```

### **3. Install GTKWave**
```sh
sudo apt install gtkwave -y
```
Verify the installation:
```sh
gtkwave --version
```

## ✅ Verification (Test Simulation)
After installation, you can test the setup with a simple Verilog design:

### **1. Create `test.v` (Sample Verilog Code)**
```verilog
module testbench;
  initial begin
    $display("Icarus Verilog & GTKWave Installed Successfully!");
    $finish;
  end
endmodule
```

### **2. Compile & Run**
```sh
iverilog -o test.out test.v
vvp test.out
```
Expected Output:
```
Icarus Verilog & GTKWave Installed Successfully!
```

## 🚀 Do’s & Don’ts
### ✅ **Do’s**
- Always **update your package manager** before installation.
- Verify installations using `iverilog -V` and `gtkwave --version`.
- Use `vvp` to run compiled Verilog files.
- Ensure **GTKWave is installed** for waveform viewing.

### ❌ **Don’ts**
- Do **not** run Verilog files directly (`./test.v` won’t work).
- Do **not** forget to clean compiled files (`rm *.out` when done).
- Do **not** assume GTKWave auto-loads files; open `.vcd` manually.

### Watch the video of installation 
![Installtion steps](Installation_steps.webm)


This setup ensures a smooth experience for Verilog development and debugging! 🚀
