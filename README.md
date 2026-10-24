# 🍽️ Smart Restaurant Digital Twin & AI Operations Platform

> **A real-time 3D Computer Vision & IoT Digital Twin for smart restaurant operations, synthetic YOLOv8 pose estimation, autonomous AGV delivery robotics, multi-camera CCTV monitoring, and executive predictive analytics.**

[![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)](https://threejs.org/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![Computer Vision](https://img.shields.io/badge/Vision-YOLOv8_Pose-emerald)](https://github.com/ultralytics)
[![Robotics](https://img.shields.io/badge/Robotics-AGV_BellaBot-blue)](https://github.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 🌟 Key Highlights & Capabilities

### 1. 🤖 Autonomous AGV Food Delivery Rover & Active Kitchen Chef NPC
* **Autonomous AGV Rover (`BellaBot` runner)**:
  * Sleek matte white & gloss obsidian chassis with dual cyan LED screen eyes that blink and smile during transit.
  * Three-tiered food serving shelves, glowing amber under-chassis neon ground strip, and a rotating top LiDAR scanner beacon.
  * Autonomous state machine: dispatches from the kitchen pass pick-up station, navigates restaurant waypoints to deliver meals to waiting diners, and returns smoothly to base.
* **Active Kitchen Chef NPC**:
  * Realistic executive double-breasted jacket, pleated tall toque hat, and dark apron.
  * Continuously animated chopping at prep counters, stirring simmering pans, plating dishes onto the pass, and ringing the service counter bell when food is ready.

### 2. 🎯 YOLOv8 Pose Skeleton Tracking & Footfall Density Heatmap
* **Synthetic YOLOv8 Pose Skeleton HUD**:
  * Real-time 2D joint coordinate projection onto an interactive SVG overlay for all active patrons, servers, and chefs.
  * Renders glowing emerald joints and connecting skeletal bone segments (shoulders, elbows, wrists, hips, knees, ankles) alongside dynamic speed vectors and posture confidence tags (`CONF: 96.8%`).
  * Toggleable via the top navigation bar **"Skeleton"** button or `K` key.
* **Spatial Footfall Density Heatmap**:
  * Trajectory tracing accumulating footfall positions onto an in-memory spatial grid canvas with multi-tier radial gaussian gradients (cyan $\to$ emerald $\to$ gold $\to$ crimson).
  * Toggleable via the top navigation bar **"Heatmap"** button or `H` key.

### 3. 📹 Multi-Camera CCTV 4-Split Grid Matrix
* **5 Switchable Real-Time Camera Modes**:
  * **CAM-01 (Ceiling AI Overview)**: Wide top-down perspective with high spatial coverage.
  * **CAM-02 (Kitchen Pass & Chef)**: Dedicated view of kitchen prep counters, chef activities, and food pick-up staging.
  * **CAM-03 (Host Stand / Entrance)**: Doorway reception monitoring patron arrivals and departures.
  * **CAM-04 / Orbit**: Free-flying interactive 3D perspective with smooth camera rotations.
  * **QUAD (4-Split CCTV Wall)**: Hardware-accelerated Three.js scissor rendering splitting the screen into 4 simultaneous real-time CCTV streams with camera labels, REC recording indicators, and timestamp watermarks.

### 4. 📊 Executive Operations Dashboard & AI Copilot
* **Dual Wait-Time Tracking**:
  * Separates **Time to Order** (seated until waiter takes order) and **Time to Food** (order placed until meal delivery).
* **Real-Time SVG Trend Sparklines**:
  * Smooth dynamic SVG graphs tracking order wait-time and food prep wait-time trajectories with min/avg/max statistics.
* **AI Operations Copilot**:
  * Predictive staffing and floor optimization recommendations calculated dynamically based on current queue depth, server load, and table turn rates.
* **Real-Time Business Metrics**:
  * Day's cumulative revenue, active guest count, average table turnover, queue length, and customer satisfaction index.

---

## 🚀 Quickstart Guide

This project is built with zero build steps or heavy node dependencies—run it directly in any modern browser!

### Option 1: Python One-Liner (Recommended)
```bash
# Clone the repository
git clone https://github.com/MrTBK/smart-restaurant-digital-twin.git
cd smart-restaurant-digital-twin

# Start local server
python3 -m http.server 3000
```
Open **`http://localhost:3000/index.html`** in your browser.

### Option 2: Node / `npx serve`
```bash
npx serve -l 3000 .
```

### Option 3: Direct File Opening
Double-click `index.html` or open it directly in Chrome, Firefox, Safari, or Edge.

---

## 🕹️ Controls & Navigation

| Control | Action |
| :--- | :--- |
| **Mouse Left Drag** | Orbit & rotate 3D camera |
| **Mouse Right Drag** | Pan camera position |
| **Mouse Wheel** | Zoom in / Zoom out |
| **Executive Dashboard Button / `D`** | Slide open the clean executive analytics drawer |
| **CAM-01 / 02 / 03 / QUAD / Orbit** | Switch CCTV perspective or multi-split video wall |
| **Heatmap Toggle / `H`** | Toggle pedestrian footfall density heatmap |
| **Skeleton Toggle / `K`** | Toggle YOLOv8 Pose joint skeleton overlay |
| **+ Party** | Manually spawn a new dining party at the host stand |
| **🔥 Rush Hour** | Toggle high-traffic lunch/dinner surge mode |

---

## 🏗️ Architecture & Technology Stack

* **Graphics Engine:** [Three.js r128](https://threejs.org/) (WebGL rendering, multi-viewport scissor testing, custom PBR-inspired lighting, shadows, and materials)
* **Animation Engine:** [GSAP](https://greensock.com/gsap/) (Smooth easing and camera transitions)
* **Styling & UI:** [Tailwind CSS](https://tailwindcss.com/) (Pure white executive glassmorphic drawer & HUD, tabular typography)
* **AI & Simulation:**
  * Client arrival Poisson process and queue dispatching
  * Finite State Machine (FSM) for Patrons, Waitstaff, Chef, and Delivery Rover
  * 3D-to-2D screen-space raycasting and joint projection
  * Dynamic SVG path smoothing for live trend sparklines

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
