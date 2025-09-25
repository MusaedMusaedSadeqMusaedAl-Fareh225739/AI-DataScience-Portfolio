AI-Driven Plant Analysis
<img align="left" src="./npec_logo.png" alt="NPEC Logo" width="120"/>

Client: Netherlands Plant Eco-phenotyping Centre (NPEC)

This project focused on identifying and segmenting root structures in Petri dish images using computer vision and automating precise plant inoculation with robotics.
By combining U-Net-based semantic segmentation with robot control (PID & RL), the project delivered an end-to-end AI-driven pipeline for plant phenotyping.

Project Highlights

Developed a U-Net model achieving F1 score = 0.85 for root mask prediction.

Applied Dijkstra’s algorithm for precise measurement of primary root length.

Automated inoculation using the OT-2 robot, comparing PID controller vs. Reinforcement Learning.

Delivered an integrated system combining vision-based analysis with robotic automation.

Key Takeaways

Gained advanced expertise in computer vision for agriculture (semantic segmentation, instance segmentation).

Built a precision robotic system for plant inoculation (<1 mm accuracy).

Conducted a comparative study of PID vs RL controllers:

PID → higher accuracy, more stable (<1 mm error).

RL → faster but slightly less accurate.

Designed and implemented a full AI-driven workflow, from image preprocessing → segmentation → measurement → robotic inoculation.

Technical Workflow

Image Processing & Segmentation

Preprocessed Petri dish images to remove background interference.

U-Net trained on refined datasets for seed, shoot, and root segmentation.

Instance segmentation enabled root length measurement and root tip detection.

Root Measurement

Applied Dijkstra’s algorithm for calculating primary root length.

Produced interpretable outputs for biological researchers.

Robotic Inoculation

Integrated computer vision outputs with OT-2 robot.

Implemented PID controller for precision liquid handling.

Compared PID vs RL for liquid delivery: accuracy vs speed trade-offs.

Planned Additions

Explanation of PID controller design (with diagrams).

Example images to illustrate workflow:

Original Petri dish image.

Plant segmentation masks.

Root structure predictions.

Inoculation targeting via robot.

Tools & Technologies

Computer Vision: U-Net, OpenCV, Dijkstra’s algorithm

Deep Learning: PyTorch / TensorFlow

Robotics: OT-2 robot, PID controller, Reinforcement Learning agent

Visualization: Matplotlib, Seaborn

Automation: Integration of CV pipeline with robot API

Authors

Musaed Al-Fareh – AI Engineer / Data Science Student at BUas
