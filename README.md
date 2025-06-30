- 🇰🇷 [한국어 (Korean)](./README.ko.md)

# Hyfeast

**Hyfeast** is a high-performance finite element analysis (FEA) framework freely available for structural analysis and design applications.

This repository provides a distribution package including binaries, manuals, and example input files.

> 🔗 Download the latest version from the [Releases](https://github.com/jrcho/Hyfeast/releases/latest) page.

To view the Hyfeast help documentation in your browser, visit:

👉 [https://jrcho.github.io/Hyfeast/index.html](https://jrcho.github.io/Hyfeast/index.html)

## System Requirements

- Windows 10 or higher
- 64-bit system
- (Optional) Python 3.8 or higher

## How to Use

1. Download the latest release from the [Releases](https://github.com/jrcho/Hyfeast/releases/latest) page.
2. Extract the ZIP file.
3. Run `bin/hyfeast.exe`.
4. Refer to `docs/manual.pdf` for instructions or run the example cases.

## Documentation

- `docs/manual.pdf`: Full feature manual
- `docs/help.html`: GUI Help (optional)
- `examples/`: Sample input files for various cases

## Third-Party Libraries Used in Hyfeast

Hyfeast leverages a variety of open-source and third-party libraries to support its high-performance finite element analysis and visualization capabilities.

### Math Kernel & Solvers

- **Intel OneAPI MKL** – Math kernel library with BLAS, LAPACK, and fast vector/matrix operations  
- **PARDISO** – Direct sparse solver (included in MKL)  
- **ARPACK** – Eigenvalue solver for large sparse systems  
- **EIGEN** – Lightweight C++ template library for linear algebra and QR solver  
- **HDF5** – High-performance data format for storing large scientific datasets

### C++ Libraries and Core Framework

- **HFC** – In-house finite element class library used across Hyfeast modules

### GUI & Visualization

- **Qt** – GUI toolkit for user interface  
- **VTK (Visualization Toolkit)** – 3D graphics and visualization engine  
- **NETGEN** – 2D mesh generator

### Misc. External Libraries

- **xlnt** – C++ library for Excel .xlsx file I/O  
- **RapidJSON** – Fast JSON parser/generator for C++  
- **JKQtPlotter** – Qt-based scientific plotting widget

### External Tools (Optional)

- **Pandoc** – Document converter used for generating formatted output  
- **ezdxf (Python)** – Python library for DXF export used in `hfVisualizer`  
  - Installation: `pip install ezdxf`

For licensing and attribution details, refer to the `LICENSE.txt` file.

## License

This software is provided under a custom license.  
See the [LICENSE.txt](LICENSE.txt) file in this repository for full terms.

## Contact

Official contact and technical support: jrcho2012@gmail.com
