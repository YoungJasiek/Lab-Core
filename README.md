# LabCore (LabCore.dll)

[![Engine: Lab](https://img.shields.io/badge/Engine-Lab-blue?style=for-the-badge)](https://github.com/YoungJasiek/Lab)
[![Online Documentation](https://img.shields.io/badge/Docs-VDC%20Online-green?style=for-the-badge)](https://youngjasiek.github.io/Lab/module-core.html)
[![Artifact](https://img.shields.io/badge/Output-LabCore.dll-blueviolet?style=for-the-badge)](https://github.com/YoungJasiek/lab-core)

Core engine lifecycle, windowing, Win32/GLFW input handling, vector math, camera transforms, dialogs, and font atlas rendering.

---

## đź“– Online Documentation
Full API references, class diagrams, subsystem architecture, and integration tutorials are published on the official documentation portal:
đź‘‰ **[https://youngjasiek.github.io/Lab/module-core.html](https://youngjasiek.github.io/Lab/module-core.html)**

---

## đź“¦ Exported Headers
- `LabCore.h`
- `LabMath.h`
- `LabCamera.h`
- `LabFont.h`
- `LabDialogs.h`
- `LabExport.h`

---

## âš™ď¸Ź Standalone Build Instructions
Compile this module independently into `LabCore.dll`:
``powershell
mkdir build
cd build
cmake .. -A x64
cmake --build . --config Release
``

Precompiled binaries are output to `build/Release/LabCore.dll`.

---
Â© 2026 YoungJasiek. Licensed under the MIT License.
