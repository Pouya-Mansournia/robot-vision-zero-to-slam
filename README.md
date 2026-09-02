# Robot Vision: Zero to SLAM

A free, bilingual (English / فارسی) book that takes you from "what is a digital image?" to a working robot vision stack: pixels, filters, edges, features, camera geometry, YOLO, deep learning, and finally Visual SLAM and ROS 2.

The whole book is plain HTML. There is nothing to install and nothing to build. Open a file in a browser and read, or read it online once GitHub Pages is turned on.

## What you will learn

The book follows the path a computer vision engineer actually walks, one chapter at a time. Each chapter assumes you understood the previous one.

- How an image is stored as a matrix of numbers, and how to build and change one with NumPy
- The classical toolbox: convolution, blur, thresholding, histograms, morphology, gradients, Canny, contours
- Feature detection and matching (Harris, ORB) and why it is the basis of panoramas, visual odometry, and SLAM
- Camera geometry: the pinhole model, the camera matrix, calibration, and stereo depth
- Object detection with YOLO, including IoU, NMS, dataset and label formats, COCO, and the YOLO family up to recent versions
- How a CNN learns its own filters, semantic segmentation, and transfer learning
- Visual odometry, optical flow, Visual SLAM, and sensor fusion with a Kalman filter
- Running vision in ROS 2: nodes and topics, `cv_bridge`, QoS, RGB-D synchronization, and the latency/FPS trade-offs behind a real-time system

## Who it is for

People who can read basic Python and want to understand robot vision from the ground up rather than copy-paste a detection script. No prior computer vision, linear algebra course, or math background is assumed. Terms are defined where they first appear and repeated in a glossary at the end of each chapter.

## Chapters

| # | Chapter | Part |
|---|---------|------|
| 1 | What Is a Digital Image? | Image Foundations |
| 2 | OpenCV From Scratch | Image Foundations |
| 3 | Classical Image Processing | Classical Vision |
| 4 | Edges and Shapes | Classical Vision |
| 5 | Feature Detection & Matching | Classical Vision |
| 6 | Camera Geometry & 3D Vision | Classical Vision |
| 7 | Object Detection with YOLO | Deep Learning |
| 8 | Deep Learning for Vision | Deep Learning |
| 9 | Vision for Robotics | Vision on a Real Robot |
| 10 | ROS 2 and Real-Time Vision | Vision on a Real Robot |

`index.html` is the table of contents and links every chapter in order.

## How to read it

Start at `index.html` or open `01-what-is-a-digital-image.html` directly. Read the chapters in order. Each one has:

- "Try it yourself" boxes with code you can copy, run, and check against the expected output
- A "Common mistakes" section near the end
- A glossary, linked from every technical term in that chapter via footnotes

Use the toggle in the header to switch between English and Persian, and between light and dark themes. Your choice is saved in the browser.

## Reading online

The book is a set of static pages, so it works as a GitHub Pages site with no configuration. Enable Pages in the repository settings (branch `main`, root folder) and it will be served at:

```
https://pouya-mansournia.github.io/robot-vision-zero-to-slam/
```

Until then, clone or download the repository and open the files locally:

```bash
git clone https://github.com/Pouya-Mansournia/robot-vision-zero-to-slam.git
cd robot-vision-zero-to-slam
# open index.html in your browser
```

## Running the code samples

The code in the book is written for Python 3 with the standard vision stack. The chapters use, in order of appearance:

- NumPy and OpenCV (`opencv-python`)
- PyTorch, for the deep learning chapters
- Ultralytics YOLO, for Chapter 7
- ROS 2 and `cv_bridge`, for Chapter 10

Each chapter names the packages it needs where it needs them. There is no single requirements file, because the dependencies grow as the book progresses and Chapter 10 in particular expects a working ROS 2 setup.

## Repository structure

```
robot-vision-zero-to-slam/
├── index.html                        table of contents
├── 01-what-is-a-digital-image.html
├── 02-opencv-basics.html
├── 03-classical-image-processing.html
├── 04-edges-and-shapes.html
├── 05-feature-detection.html
├── 06-camera-geometry-3d-vision.html
├── 07-object-detection-yolo.html
├── 08-deep-learning-vision.html
├── 09-robot-vision-slam-fusion.html
└── 10-ros2-realtime-inference.html
```

Each HTML file is self-contained. Fonts and the KaTeX math stylesheet load from a CDN, so math renders best with an internet connection.

## Status and limitations

- All 10 chapters are written and readable in both languages.
- The code samples are meant to be run and read alongside the text. They are not packaged as a test suite or a runnable project.
- There is no dependency lock file or CI.
- Chapter 10 assumes you already have ROS 2 installed; the book does not cover that install.
- The book has not been chosen a formal license yet. Until a `LICENSE` file is added, "free" means free to read, not a grant of reuse rights. A Creative Commons license (for the prose) is the likely choice.

## Contributing

Corrections and clearer explanations are welcome. Open an issue describing the chapter, the section, and what is wrong or unclear, or send a pull request with the edit. Please keep both the English and Persian versions of any changed passage in sync.

## Author

Pouya Mansournia
