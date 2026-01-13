# 📸 Webcam Studio: Capture, Zoom & Rotate

A robust, client-side web application designed for high-quality image acquisition directly from your browser. This tool provides a "studio-style" interface that separates the live camera feed from the captured result, allowing for precise adjustments and hardware-level control.

## 📖 Description

The **Webcam Studio** is a lightweight, single-page utility that transforms any standard webcam into a versatile capture tool. Unlike standard camera apps, it provides granular control over the hardware and post-capture orientation.

### Key Features
* **Split-Pane Workflow:** View your live stream in a high-resolution viewport while reviewing captured "stills" in a dedicated preview pane.
* **Hardware-Level Zoom:** Direct integration with the camera's internal motor or digital zoom (via the `MediaStreamTrack` API), allowing for close-up shots without losing initial sensor data.
* **Lossless Rotation:** Captured images can be rotated in 90-degree increments. The application re-renders the image onto a dynamic canvas to ensure the saved file maintains the correct orientation.
* **Smart Power & Privacy:** Features a built-in **Inactivity Watchdog**. If no interaction is detected for 5 minutes, the app automatically kills the camera stream to protect privacy and save power.
* **High-Quality Output:** Exports images in JPEG format with a 0.95 quality rating, balancing file size with professional clarity.

---

## 💡 Enhancing Quality with WebVAC

While this application captures the best raw feed your hardware can provide, web-based captures are often limited by sensor noise or browser compression.

> [!TIP]
> **To achieve professional-grade resolution:** We strongly recommend processing your saved JPEGs through an **external WebVAC (Web-based Video/Audio Converter or Upscaler)**. Using an external WebVAC can:
> * **Increase Resolution:** Upscale 720p or 1080p captures to 4K using AI.
> * **Denoise:** Remove the "grain" typical of low-light webcam sensors.
> * **Sharpen:** Recover fine details that standard browser interpolation might miss.

---

## 🛠 Technical Specifications

This project is built using a "No-Framework" philosophy, utilizing native Web APIs for maximum performance and zero dependencies.

| Feature | Specification |
| :--- | :--- |
| **Canvas Resolution** | $1280 \times 960$ (4:3 Aspect Ratio) |
| **Export Format** | `image/jpeg` |
| **JPEG Quality** | 95% |
| **Idle Timeout** | 300 seconds (5 minutes) |
| **Compatibility** | Chrome, Edge, Opera (Browsers supporting Image Capture API) |

### APIs Used
* `getUserMedia()`: Accesses the video stream.
* `ImageBitmap`: Handles efficient image data for rotation.
* `applyConstraints()`: Passes zoom values directly to the camera hardware.

---

## 🚀 How to Use

1.  **Clone/Download:** Save the `index.html` file to your local machine.
2.  **Launch:** Open the file in a modern web browser (Chrome or Edge recommended).
3.  **Capture:**
    * Adjust the **Zoom** slider to frame your shot.
    * Click **Take Picture** (or use the `S` access key).
    * **Rotate** the result if necessary.
4.  **Save:** Click **Save Picture** to download the final JPEG.

---

## 🤝 Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any enhancements—such as adding filters, multi-camera toggles, or timer functions—are greatly appreciated.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---
