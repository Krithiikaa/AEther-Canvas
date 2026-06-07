<div align="center">

# 🌌 Æther Canvas

<img src="https://media.giphy.com/media/l41lFw057lFZ3QCmQ/giphy.gif" width="120" alt="Neon Space Planet" />

### *Paint upon the invisible. Your hand becomes the brush.*

<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMmVoejJrcmkyMjg1MWp2dWswbjM5dzZlMmNyeDNhczhsbXBmdnVjZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/T3VvkObtEPRTsp2wdU/giphy.gif" width="80" alt="Neon Sparkles" />

<p align="center">
  <img src="https://img.shields.io/badge/Style-Neon%20Aesthetic-bf5af2?style=for-the-badge&logoColor=white" alt="Style Badge" />
  <img src="https://img.shields.io/badge/Air%20Painting-MediaPipe-007acc?style=for-the-badge&logo=google&logoColor=white" alt="MediaPipe Badge" />
  <img src="https://img.shields.io/badge/Rendering-Hardware%20Accelerated-4ade80?style=for-the-badge&logoColor=white" alt="Rendering Badge" />
  <img src="https://img.shields.io/badge/Splines-Quadratic%20Bezier-c084fc?style=for-the-badge&logoColor=white" alt="Splines Badge" />
</p>

---

[✨ Live Demo](https://github.com/Krithiikaa/AEther-Canvas) • [📝 Implementation Plan](file:///C:/Users/User/.gemini/antigravity-ide/brain/b5a37137-08a9-4850-b6e8-7a2bc6af900e/implementation_plan.md) • [🚀 Walkthrough](file:///C:/Users/User/.gemini/antigravity-ide/brain/b5a37137-08a9-4850-b6e8-7a2bc6af900e/walkthrough.md)

</div>

---

## 💫 The Experience
**Æther Canvas** is a premium, browser-based digital painting canvas that uses real-time computer vision to track hand movements, translating your physical gestures into high-fidelity neon artwork. No mouse, no touch screens, no physical controllers—just you, the air, and your imagination.

---

## ⚡ Engineered for Performance & Elegance

Unlike standard computer-vision canvas applications that experience lag, coordinate jagginess, or opacity overlapping bugs, **Æther Canvas** is engineered with a custom rendering pipeline:

*   **🎬 60 FPS Native Camera Loop**: Uses a direct webcam hardware stream integrated with the modern `requestVideoFrameCallback` API. Frames are processed the exact millisecond they are decoded, eliminating legacy polling latency.
*   **🥞 Dual-Canvas Overlay Rendering**: The application keeps active drawing strokes separated on a transparent **Overlay Canvas (`#tc`)** and only flushes them to the permanent **Background Canvas (`#gc`)** when the stroke is committed. This solves the HTML5 Canvas "beading" transparency bug, ensuring perfectly uniform stroke opacity.
*   **📈 Quadratic Bezier Smoothing**: Incorporates real-time math-based spline interpolation (`quadraticCurveTo`) through segment midpoints. Hand tremors and tracker jitter are smoothed away, producing elegant, calligraphic vector lines.
*   **🎭 Gesture Hysteresis (Grace Period)**: Includes a `350ms` debouncing bridge that maintains the drawing stroke during minor tracking drops or flinches, avoiding thread-blocking CPU saves.

---

## 🖐️ Magic Gestures

<div align="center">
  <img src="https://media.giphy.com/media/du3J3JHdDsYMClIO0F/giphy.gif" width="120" alt="Drawing Hand Animation" />
</div>

| Gesture | Cursor | Action | Description |
| :---: | :---: | :---: | :--- |
| **☝️** | `☝️` | **Draw** | Lift only your index finger. Paint a glowing neon path. |
| **🖐️** | `🧽` | **Erase** | Open your entire palm. Cleanly wipe away strokes. |
| **✊** | *(Hidden)* | **Pause / Lift** | Make a closed fist to lift the brush or pause detection. |

---

## 🎨 Premium UI Controls
-   🌌 **Vibrant HSL Palette**: Harmonious neon presets alongside custom full-spectrum color pickers.
-   ✏️ **Configurable Brush Mechanics**: Real-time sliders to customize stroke thickness, neon glow radius, and EMA smoothing strength (down to `0%` for raw hand speed).
-   🪞 **Symmetrical Mirror Mode**: Draw and erase symmetrically on both sides of the mirror plane.
-   ⚡ **Show Camera Preview**: Toggle a clean, scale-reversed camera preview window at the corner of your screen.
-   💾 **Actions**: Quick clear, undo/redo stroke buffers, and save your masterpieces as high-resolution transparent PNG files.

---

## 🚀 Quick Setup & Run

No installations required. Since it's built with pure, modern vanilla web standards, you can run it locally in seconds:

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/Krithiikaa/AEther-Canvas.git
    cd AEther-Canvas
    ```
2.  **Start a Local Server**:
    *Using Python (standard)*:
    ```bash
    python -m http.server 8000
    ```
3.  **Explore**:
    Open **[http://localhost:8000](http://localhost:8000)** in Chrome, Edge, or Safari, grant camera permissions, and raise your hand!

---

<div align="center">
  <img src="https://media.giphy.com/media/3orif2CsQ1qNfip21y/giphy.gif" width="80" alt="Neon Drawing Pencil" />
  
  *Created with ❤️ by Krithiikaa. Paint the invisible.*
</div>