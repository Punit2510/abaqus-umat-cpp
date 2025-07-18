# 🔩 Abaqus UMAT Subroutine in C++ with Eigen Integration

This repository provides a C++ implementation of a *UMAT (User Material Subroutine)* for *Abaqus Standard, used for modeling a 3D linear elastic isotropic material. The subroutine uses the **Eigen* C++ library for matrix operations and is compiled using *Microsoft Visual Studio (MSVS)* along with the *Intel compiler*.

---

## 🧩 Features

- Custom material model defined using a C++ UMAT subroutine.
- Integration with *Eigen* library for efficient matrix operations.
- Compatible with Abaqus .inp files for user-defined material analysis.
- Easy visualization of simulation results in *Abaqus CAE*.

---

## 🛠 Requirements

- Microsoft Visual Studio (MSVS)
- Intel C++/Fortran Compiler (linked with Abaqus)
- Abaqus CAE
- Eigen Library (Header-only)

---

## 🚀 Getting Started

### 1. Compile the UMAT C++ Code

Open the *MSVS Developer Command Prompt* and run:

```bash
cl /c /O2 /I"path\to\eigen" umat.cpp
> Replace path\to\eigen with the actual path to your Eigen folder.  
> This will generate an object file umat.obj.

---

### 2. Run the Abaqus Simulation

Once the .obj file is generated, use the Abaqus Command Prompt to execute the simulation:

```bash
abaqus job=umat user=umat.obj interactive

This will run the analysis defined in the umat.inp input file.

After the simulation is complete, you can visualize the results in Abaqus CAE using:

abaqus cae database=umat.odb
