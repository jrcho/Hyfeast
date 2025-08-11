# Hyfeast

**Hyfeast** is a high-performance finite element analysis (FEA) framework developed by the Korea Institute of Civil Engineering and Building Technology (KICT).  It is freely available for structural analysis and design applications. 

Hyfeast supports shell, beam, and solid elements, fast parallelized solving, 3D visualization, and batch-mode analysis. It is designed for researchers, engineers, and developers working in structural mechanics and design automation.

- Download: [Latest release](https://github.com/jrcho/Hyfeast/releases/latest)  
- Help: [Online documentation](https://jrcho.github.io/Hyfeast/index.html)  
- Korean version: [README.ko.md](./README.ko.md)

## System Requirements

- 64-bit Windows 10 or higher
- [Microsoft Visual C++ Redistributable for Visual Studio 2015–2022 (x64)](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)  
  (Required to run Hyfeast programs built with Visual Studio)
- (Optional) Python 3.8 or higher (for DXF import)

## Installation and Usage

1. Download the latest release from the [Releases](https://github.com/jrcho/Hyfeast/releases/latest) page.
2. Extract the ZIP file to any location (e.g., `Hyfeast/`).
3. Open the `Hyfeast` folder and double-click `setpath.bat`, which sets the PATH environment variable and opens a command prompt.
4. In the command prompt, you can run:
   ```
   Hyfeast> hfVisualizer
   Hyfeast> hfAnalyzer input.inp
   Hyfeast> hfSectionVisualizer
   Hyfeast> hfSectionAnalyzer input.sec
   ```

Refer to the manual or examples for usage details.

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

- Python – Use for running ezdxf, and modal identification scripts
- ezdxf (Python) – DXF export for `hfVisualizer`
- Pandoc – Document converter  



See `LICENSE.txt` for full licensing and attribution details.


## License

This software is provided under a custom license.  
Refer to the `LICENSE.txt` file for full terms and conditions.



## Contact

For questions or technical support: jrcho2012@gmail.com
