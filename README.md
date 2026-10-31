# Hyfeast

**Hyfeast** is a high-performance finite element analysis (FEA) framework developed by the Korea Institute of Civil Engineering and Building Technology (KICT).  It is freely available for structural analysis and design applications. 

Hyfeast supports shell, beam, and solid elements, fast parallelized solving, 3D visualization, and batch-mode analysis. It is designed for researchers, engineers, and developers working in structural mechanics and design automation.

- Download: [Latest release](https://github.com/jrcho/Hyfeast/releases/latest)  
- Help: [Online documentation](https://jrcho.github.io/Hyfeast/index.html)  
- Offline help: `Bin\help\index.html`  
- Korean version: [README.ko.md](./README.ko.md)

## System Requirements

- 64-bit Windows 10 or higher

## Installation and Usage

Hyfeast runs straight from the extracted folder. Running `install.bat` once adds Start menu entries and commands so that it is easier to use.

### 1. Extract

1. Download the latest release from the [Releases](https://github.com/jrcho/Hyfeast/releases/latest) page.
2. Extract the ZIP file to any location (e.g., `D:\Apps\Hyfeast-v1.0.0`). Below, this folder is called the **distribution folder**.

### 2. Install (recommended)

Double-click `install.bat` in the distribution folder. No administrator rights are needed, and no files are copied elsewhere.

- A Start menu folder named after the distribution folder (e.g., `Hyfeast-v1.0.0`) gets hfStudio, hf2DStudio, Hyfeast Command Prompt, Hyfeast Help, Examples and Uninstall.
- The installer asks whether to create desktop shortcuts.
- The commands `hfAnalyzer`, `hfSectAnalyzer`, `hfStudio` and `hf2DStudio` are registered. In any command prompt or PowerShell window opened **after** installing, they run from any folder.

```
D:\Work\proj> hfAnalyzer frame.inp
D:\Work\proj> hfStudio
```

If you move the distribution folder, the shortcuts break; run `install.bat` again in the new location.

### 3. Use without installing

Double-click `HyfeastCmd.bat` in the distribution folder to open a command prompt with the Hyfeast environment. To set the environment in a command prompt that is already open, type:

```
D:\Work\proj> D:\Apps\Hyfeast-v1.0.0\HyfeastCmd.bat --no-shell
D:\Work\proj> hfAnalyzer frame.inp
```

### 4. Several versions

- Running `install.bat` for each version gives each its own Start menu folder.
- Commands such as `hfAnalyzer` run the **most recently installed** version.
- To use another version in one window, run that version's `HyfeastCmd.bat --no-shell`; it takes precedence in that window.
- `where hfAnalyzer` shows which program will run.

### 5. Uninstall

Run **Uninstall** from the Start menu or `uninstall.bat` in the distribution folder to remove the shortcuts and commands and to reset the hfStudio and hf2DStudio settings (`*.ini` in `Bin`). The `.hyfeast` work folders (autosave backups and similar) in the distribution folder and in `Bin` are also deleted. The commands are removed only if they point to this version. The DigitalTwin activation is shared by all versions and is kept. Close hfStudio and hf2DStudio first so that the settings can be reset. Then delete the distribution folder.

Refer to the Help or examples for usage details.

## Third-Party Libraries Used in Hyfeast

Hyfeast incorporates the following open-source and third-party libraries:

### Math Kernel & Solvers

- Intel OneAPI MKL – BLAS, LAPACK, vector operations  
- PARDISO – Direct sparse solver (part of MKL)  
- ARPACK – Eigenvalue solver for sparse systems  
- Eigen – C++ linear algebra library  
- HDF5 – Scientific data storage format

### GUI & Visualization

- Qt – GUI framework  
- VTK – 3D visualization engine  
- NETGEN – 2D mesh generator

### Utilities

- xlnt – Excel `.xlsx` I/O library for C++  
- RapidJSON – JSON parser for C++  
- JKQtPlotter – Qt-based scientific plotting

### External Tools (Optional)

- Python – Use for running Digital Twin/OMA analysis scripts
- Pandoc – Document converter  



See `LICENSE.txt` for full licensing and attribution details.


## License

This software is provided under a custom license.  
Refer to the `LICENSE.txt` file for full terms and conditions.



## Contact

For questions or technical support: jrcho2012@gmail.com
