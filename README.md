# VSD Tools Setup & Installation

This document describes the installation process for open-source tools used in VLSI design. Each section provides commands, verification steps, and space for screenshots.

---

## 1. System Requirements

- **Operating System:** Ubuntu 20.04 LTS or newer  
- **RAM:** Minimum 6 GB (8 GB recommended)  
- **Disk Space:** 50 GB free  
- **Processor:** 4 cores or more  

---

## 2. Tools Covered

- Yosys (Synthesis)  
- Icarus Verilog (Simulation)  
- GTKWave (Waveform Viewer)  
- NGSpice (Circuit Simulation)  
- Magic VLSI (Layout Design)  

---

## A. Yosys – RTL Synthesis

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex    libreadline-dev gawk tcl-dev libffi-dev git    graphviz xdot pkg-config python3 libboost-system-dev    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
git submodule update --init --recursive
make
sudo make install
```

**Verification:**  
```bash
yosys
```

📸 *[Insert Yosys Screenshot Here]*  

---

## B. Iverilog – Verilog Simulation

```bash
sudo apt-get install iverilog
```

**Verification:**  
```bash
iverilog
```

📸 *[Insert Iverilog Screenshot Here]*  

---

## C. GTKWave – Waveform Viewer

```bash
sudo apt update
sudo apt install gtkwave
```

**Verification:**  
```bash
gtkwave
```

📸 *[Insert GTKWave Screenshot Here]*  

---

## D. NGSpice – Circuit Simulator

```bash
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release && cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install
```

**Verification:**  
```bash
ngspice
```

📸 *[Insert NGSpice Screenshot Here]*  

---

## E. Magic VLSI – Layout Tool

```bash
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev    libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```

**Verification:**  
```bash
magic
```

📸 *[Insert Magic Screenshot Here]*  

---

## 3. Version Checks

Run these commands to confirm tool versions:

```bash
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
```

📸 *[Insert Version Screenshot Here]*  

---

## 4. Installation Summary

| Tool       | Status   | Purpose            |
|------------|----------|--------------------|
| Yosys      | ✅ Done  | RTL Synthesis      |
| Iverilog   | ✅ Done  | Verilog Simulation |
| GTKWave    | ✅ Done  | Waveform Debugging |
| NGSpice    | ✅ Done  | Circuit Simulation |
| Magic VLSI | ✅ Done  | Layout Design      |
| Versions   | ✅ Done  | Environment Check  |

---

## Credits

- **Contributor:** Tharun Babu V  
- **Program:** VLSI System Design (VSD)  
