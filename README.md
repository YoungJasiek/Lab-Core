# lab-core (LabCore.dll)

[![Engine: Lab](https://img.shields.io/badge/Engine-Lab-blue?style=for-the-badge)](https://github.com/YoungJasiek/Lab)
[![Online Documentation](https://img.shields.io/badge/Docs-VDC%20Online-green?style=for-the-badge)](https://youngjasiek.github.io/Lab/module-core.html)
[![Artifact](https://img.shields.io/badge/Output-LabCore.dll-blueviolet?style=for-the-badge)](https://github.com/YoungJasiek/lab-core)

Foundational engine subsystem providing application lifecycle, deterministic 64Hz loop timing, Win32/GLFW input processing, vector math (Vec2, Vec3, Mat4), camera projection, native file dialogs, and font atlas rendering.

---

## 📖 Online Documentation
Full API references, class diagrams, subsystem architecture, and integration tutorials are published on the official Lab documentation portal:
👉 **[https://youngjasiek.github.io/Lab/module-core.html](https://youngjasiek.github.io/Lab/module-core.html)**

---

## 📦 Exported Headers
- `LabCore.h`
- `LabMath.h`
- `LabCamera.h`
- `LabFont.h`
- `LabDialogs.h`
- `LabExport.h`

---

## 🔗 Dependencies
- `glfw`
- `glad`
- `OpenGL::GL`
- `gdi32`
- `comdlg32`

---

## ⚙️ Standalone Build Instructions
Compile this module independently into `LabCore.dll`:
```powershell
mkdir build
cd build
cmake .. -A x64
cmake --build . --config Release
```

Precompiled binaries are output to `build/Release/LabCore.dll`.

---
© 2026 YoungJasiek. Licensed under the MIT License.
