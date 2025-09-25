# AI-Driven Plant Analysis

<img align="left" src="./npec_logo.png" alt="NPEC Logo" width="120"/>  

**Client:** Netherlands Plant Eco-phenotyping Centre (NPEC)

This project focused on **identifying and segmenting root structures** in Petri dish images using computer vision and **automating precise plant inoculation** with robotics.
By combining **U-Net-based semantic segmentation** with **robot control (PID & RL)**, the project delivered an **end-to-end AI-driven pipeline** for plant phenotyping.

---

## Project Highlights

* Developed a **U-Net model** achieving **F1 score = 0.85** for root mask prediction.
* Applied **Dijkstra’s algorithm** for precise measurement of **primary root length**.
* Automated inoculation using the **OT-2 robot**, comparing **PID controller vs. Reinforcement Learning (RL)**.
* Delivered an **integrated pipeline** combining vision-based analysis with robotic automation.

---

## Key Takeaways

* Built expertise in **computer vision for agriculture** (semantic & instance segmentation).
* Designed a **precision robotic system** for plant inoculation (<1 mm accuracy).
* Conducted a **PID vs RL comparison**:

  * **PID** → higher accuracy, stable (<1 mm error).
  * **RL** → faster but slightly less accurate.
* Developed a **complete workflow**: preprocessing → segmentation → measurement → robotic inoculation.

---

## Technical Workflow

### 1. Image Processing & Segmentation

* Preprocessed Petri dish images to remove background interference.
* Trained **U-Net** on refined datasets for **seed, shoot, and root segmentation**.
* Applied **instance segmentation** for root length measurement and root tip detection.

### 2. Root Measurement

* Used **Dijkstra’s algorithm** to calculate primary root length.
* Produced interpretable outputs for biological researchers.

### 3. Robotic Inoculation

* Integrated segmentation pipeline with the **OT-2 robot**.
* Implemented **PID controller** for precision liquid handling.
* Compared **PID vs RL** trade-offs for inoculation speed and accuracy.

---

## Planned Additions

* Detailed explanation of **PID controller design** (with diagrams).
* Example workflow images:

  * Original Petri dish image.
  * Plant segmentation mask.
  * Root prediction output.
  * Robot inoculation targeting.

---

## Tools & Technologies

* **Computer Vision**: U-Net, OpenCV, Dijkstra’s algorithm
* **Deep Learning**: PyTorch / TensorFlow
* **Robotics**: OT-2 robot, PID controller, Reinforcement Learning agent
* **Visualization**: Matplotlib, Seaborn
* **Automation**: Integration of CV pipeline with robot API

---

## Authors

* **Musaed Al-Fareh** – AI Engineer / Data Science Student @ BUas

---

