# ESP32-Cam Computer Vision

A computer vision project built around the ESP32-CAM module, using Edge Impulse for on-device
image classification. Includes camera + servo control firmware and a yellow-ball-tracking robot
that navigates a maze.

## Repository Structure

```
ESP32-Cam-Computer-Vision/
├── Codes/
│   ├── esp32_camera_RGB/                  # Base ESP32-CAM RGB streaming/capture sketch
│   ├── esp32_camera_RGB_with_servo/       # Camera + servo control for ball tracking
│   └── Collect_Images_for_EdgeImpulse/    # Scripts for capturing training images
├── Docs/
│   └── Computer_Vision_workshop_slides_2025.pdf
├── Training Data/
│   ├── Images of Yellow Ball/
│   └── Images of Yellow Ball with Maze/
├── LICENSE
└── README.md
```

## Hardware

- ESP32-CAM module
- Servo motor (for camera/steering control)
- Yellow ball target + maze course

## Getting Started

1. **Flash the firmware** — open the sketch in `Codes/esp32_camera_RGB_with_servo/` in the
   Arduino IDE, set your WiFi credentials and board settings, and upload to the ESP32-CAM.
2. **Collect training data** — use `Codes/Collect_Images_for_EdgeImpulse/` to capture yellow ball
   images from the camera feed and save them into `Training Data/`.
3. **Train the model** — upload the images in `Training Data/` to an
   [Edge Impulse](https://edgeimpulse.com/) project, label them, and train an image
   classification/object detection model.
4. **Deploy** — export the trained model back to the ESP32-CAM and run inference on-device.

## Docs

Workshop slides and reference material are in [`Docs/`](./Docs).

## License

This project is licensed under the MIT License — see [LICENSE](./LICENSE) for details.
