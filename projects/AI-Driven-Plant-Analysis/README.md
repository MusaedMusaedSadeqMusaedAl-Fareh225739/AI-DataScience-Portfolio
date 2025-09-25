# AI-Driven Plant Analysis

<img align="left" src="./npec_logo.png" alt="NPEC Logo" width="120"/>  

**Client:** Netherlands Plant Eco-phenotyping Centre (NPEC)

This project focused on **identifying and segmenting root structures** in Petri dish images using computer vision and **automating precise plant inoculation** with robotics.  
By combining **U-Net-based semantic segmentation** with **robot control (PID & RL)**, the project delivered an **end-to-end AI-driven pipeline** for plant phenotyping.

---

##  Project Highlights

- Developed a **U-Net model** achieving **F1 score = 0.85** for root mask prediction.  
- Applied **Dijkstra’s algorithm** for precise measurement of **primary root length**.  
- Automated inoculation using the **OT-2 robot**, comparing **PID controller vs. Reinforcement Learning (RL)**.  
- Delivered an **integrated pipeline** combining vision-based analysis with robotic automation.  

---

## 📌 Key Takeaways

- Built expertise in **computer vision for agriculture** (semantic & instance segmentation).  
- Designed a **precision robotic system** for plant inoculation (<1 mm accuracy).  
- Conducted a **PID vs RL comparison**:  
  - **PID** → higher accuracy, stable (<1 mm error).  
  - **RL** → faster but slightly less accurate.  
- Developed a **complete workflow**: preprocessing → segmentation → measurement → robotic inoculation.  

---

## 🔄 Workflow & Process

The pipeline integrates **computer vision + robotics** in five major steps:

---

### 1️ Original Petri Dish Image  
Captured raw plant growth images.

<p align="center">
  <img src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/AI-Driven-Plant-Analysis/Screenshot%202025-09-25%20235948.png" width="500"/>
</p>

---

### 2️ Petri Dish Extraction  
Removed background noise and isolated the dish for cleaner analysis.

<p align="center">
  <img src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/AI-Driven-Plant-Analysis/Screenshot%202025-09-25%20235736.png" width="500"/>
</p>

---

### 3️ Plant Instance Segmentation  
Applied **U-Net** for semantic segmentation of plants (seeds, shoots, roots).

<p align="center">
  <img src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/AI-Driven-Plant-Analysis/Screenshot%202025-09-25%20235743.png" width="500"/>
</p>

---

### 4️ Root Prediction  
Predicted root structures and extracted **primary root length** using **Dijkstra’s algorithm**.

<p align="center">
  <img src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/AI-Driven-Plant-Analysis/Screenshot%202025-09-25%20235751.png" width="500"/>
</p>

---

### 5️ Plant Inoculation  
Integrated predictions with the **OT-2 robot** to inoculate plants at precise root tips.  
Compared **PID controller** vs **Reinforcement Learning** for targeting accuracy.

<p align="center">
  <img src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/AI-Driven-Plant-Analysis/Screenshot%202025-09-25%20235802.png" width="500"/>
</p>

---

## Tools & Technologies

- **Computer Vision**: U-Net, OpenCV, Dijkstra’s algorithm  
- **Deep Learning**: PyTorch / TensorFlow  
- **Robotics**: OT-2 robot, PID controller, Reinforcement Learning agent  
- **Visualization**: Matplotlib, Seaborn  
- **Automation**: Integration of CV pipeline with robot API  

---

## 👥 Authors

- **Musaed Al-Fareh** – AI Engineer / Data Science Student @ BUas  
