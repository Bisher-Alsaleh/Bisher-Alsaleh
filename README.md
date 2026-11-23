<h1 align="center">Bisher Alsaleh</h1>

<p align="center">
  <b>AI & Computer Vision Engineer</b><br>
  M.Sc. Student, Computer Science for Autonomous Systems · Eötvös Loránd University (ELTE), Budapest
</p>

<p align="center">
  <i>Teaching machines to see, reconstruct, and restore the places conflict has damaged.</i>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/bisher-alsaleh"><img src="https://img.shields.io/badge/LinkedIn-Bisher%20Alsaleh-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:Bisher.Alsaleh@outlook.com"><img src="https://img.shields.io/badge/Email-Bisher.Alsaleh%40outlook.com-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="./Bisher_Alsaleh_CV.pdf"><img src="https://img.shields.io/badge/CV-PDF-2E7D32?style=flat" alt="CV"></a>
  <a href="https://link.springer.com/article/10.1007/s12555-026-00062-1"><img src="https://img.shields.io/badge/Publication-IJCAS%20(Springer)-8E24AA?style=flat" alt="Publication"></a>
</p>

---

## About

I am an M.Sc. student at Eötvös Loránd University in Budapest (2026–2028), studying on a Stipendium Hungaricum scholarship. This semester I am studying deep network development, image and signal processing, 3D computer vision, and vehicle sensing. I hold a B.Sc. in Robotics and Intelligent Systems from Manara University, graduating with Excellence (GPA 3.46/4.00, ranked 4th of 16).

My background is in 3D reconstruction, computer vision, and control for mobile robots. My undergraduate thesis was a monocular-camera robot that autonomously drives through an indoor space and reconstructs it in 3D, and I co-authored a peer-reviewed paper on neural-network-based robot control in the *International Journal of Control, Automation and Systems* (Springer). I then worked as a university teaching assistant at Manara University, teaching 150+ students and mentoring two capstone groups.

Alongside my courses, I am working on generative completion of partially reconstructed heritage sites, using 3D-conditional diffusion models. The motivation is personal: I have seen cultural landmarks destroyed by conflict, and I want people everywhere to be able to explore such places as they once were. In the long term, I want to do research and development at the intersection of 3D vision, generative models, and autonomous systems, and I am open to research collaborations and to internships and roles in these areas.

---

## Current Research · *in progress*

### Generative semantic completion of partially reconstructed heritage environments using 3D-conditional diffusion models

Reconstructing a damaged heritage site gives you what survives: fragments of geometry, missing walls, holes where a roof or a column used to be. That is a record of the damage, not of the place.
My research asks whether a generative model can **complete** these partial reconstructions, producing a plausible, semantically consistent version of the intact site, so that people can explore it virtually and understand what it was worth.

```mermaid
flowchart LR
    A[Capture<br/>images / robot / drone] --> B[Partial 3D<br/>reconstruction]
    B --> C[3D-conditional<br/>diffusion completion]
    C --> D[Semantically complete<br/>environment]
    D --> E[Interactive<br/>virtual exploration]
```

- **Problem:** reconstructions of deteriorated sites are incomplete and cannot be experienced as the intact place.
- **Approach:** condition a 3D diffusion model on the partial reconstruction to generate the missing geometry and semantics.
- **Goal:** an interactive virtual version of the restored site that conveys its past form and value.
- **Status:** early-stage research, carried out alongside my M.Sc. at ELTE. Updates will be added here as the work progresses.

The projects below are the first stage of this pipeline, **capture and reconstruction**. The research is the second: **completion**.

---

## Featured Projects

### [Autonomous 3D Mapping with a Monocular Camera](https://github.com/B-A-IntelliBots/Autonomous-3D-Mapping)
*Feb – Aug 2025 · Python, ROS, OpenCV, PCL, COLMAP, OpenMVS, Raspberry Pi, Arduino*

My undergraduate thesis (graded 4.00/4.00): an end-to-end system in which a differential-drive robot with a single camera maps an indoor space on its own.
- Deployed DISK and LightGlue inside a COLMAP/OpenMVS pipeline to produce reliable 3D scenes.
- Tuned the robot dynamics with a Genetic Algorithm and filtered feedback signals with an FIR filter for stable localization.
- Used the hybrid Lyapunov–LQR controller (see below) for path tracking.

This video shows the end-to-end autonomous 3D reconstruction process:

<div align="center">
  <video src="https://github.com/user-attachments/assets/662caa91-467a-4c62-9c5a-49453e5b212f" controls loop></video>
</div>

<div align="center">
  <table>
    <tr>
      <td rowspan="2" width="40%">
        <img src="https://github.com/user-attachments/assets/55900751-be20-40be-a148-f7c0440b624e" width="100%">
      </td>
      <td width="26%">
        <img src="https://github.com/user-attachments/assets/096c45c2-9bc9-43c6-a107-1c5f101271f1" width="100%">
      </td>
      <td rowspan="2" width="34%">
        <img src="https://github.com/user-attachments/assets/03510057-2b9b-45db-9acf-d9cadb2f2c6f" width="100%">
      </td>
    </tr>
    <tr>
      <td>
        <img src="https://github.com/user-attachments/assets/4cce0b84-d043-425a-957f-8ba96fe1a7a8" width="100%">
      </td>
    </tr>
  </table>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/889543d1-367c-475c-b36f-7b4da2a5b131" alt="Autonomous 3D mapping result" />
</div>

---

### [Hierarchical Localization & 3D Reconstruction Benchmark](https://github.com/B-A-IntelliBots/3D-Reconstruction)
*Feb – Jul 2024 · Python, HLOC, OpenCV, NumPy, Matplotlib*

A benchmark of feature extractor and matcher combinations (SuperPoint and DISK with SuperGlue and LightGlue) inside the HLOC pipeline. Each combination is scored by inlier matches and pose-estimation accuracy based on the fundamental matrix. The results guide which components give the best input for multi-view stereo and mesh generation.

<div align="center">
  <img width="100%" alt="3D reconstruction results" src="https://github.com/user-attachments/assets/ffd49e92-56b4-43b8-a0fb-b6192f1f8d93" />
  <img width="80%" alt="Extractor and matcher comparison" src="https://github.com/user-attachments/assets/c873e968-21fb-49c0-9423-00bcf1dd3c3d" />
</div>

---

### [CulturalVision: Landmark Recognition with YOLOv8](https://github.com/Bisher-Alsaleh/CulturalVision-YOLOv8n-CL-FineTune)
*Sep – Oct 2025 · PyTorch, Ultralytics YOLOv8, pandas, scikit-learn*

A lightweight model for recognizing cultural landmarks, built to support heritage documentation.
- Built the data pipeline: the 10 most frequent classes of Google Landmarks Dataset v2, up to 900 images per class (~9,000 total), and a stratified 80/20 split with fixed seeds.
- Fine-tuned YOLOv8n-cls (AdamW, cosine learning rate, 24 epochs, 224 px) to **97.9% top-1 validation accuracy**.
- Released modular training, evaluation, and inference scripts, with the dataset and weights on Kaggle.

<div align="center">
  <img src="./images/CulturalVision.png" width="55%" alt="CulturalVision: landmark classification with YOLOv8" />
</div>

---

### [AI-Optimized LQR–Lyapunov Control System](https://github.com/B-A-IntelliBots/AI-optimized-LQR-Lyapunov-Control-System)
*Nov 2024 – Jan 2025 · MATLAB, Simulink, Gazebo, Python*

A hybrid controller for a differential-drive robot: Lyapunov control with gains selected by an MLP, combined with LQR and a state observer. The MLP was trained on simulated data, and the controller was compared against standard controllers in MATLAB and Gazebo.

<div align="center">
  <img width="320" alt="Discretized path tracking" src="https://github.com/user-attachments/assets/437ce3ed-46cc-4fcd-a637-b37ed2ebe77c" />
</div>

---

## Publication

**A. Deeb, B. Alsaleh, I. Hatem (2026).** *AI-Driven Control Strategy for DDWMR: Neural Network-Based Parameter Optimization and Real-Time Stabilization for Multi-Waypoint Navigation.* International Journal of Control, Automation and Systems (IJCAS), Springer. [Read the paper on Springer Link](https://link.springer.com/article/10.1007/s12555-026-00062-1)

---

## Education

**M.Sc. Computer Science for Autonomous Systems** · Eötvös Loránd University, Budapest · Sep 2026 – Sep 2028
Stipendium Hungaricum scholar. Current courses: Deep Network Development, Image and Signal Processing, 3D Computer Vision, Introduction to Vehicles and Sensors.

**B.Sc. Robotics and Intelligent Systems** · Manara University, Latakia, Syria · Nov 2020 – Aug 2025
GPA 3.46/4.00 (89.2%, Excellence), ranked 4th of 16. Coursework included Machine Learning, Deep Learning, Computer Vision, and Digital Signal Processing.

---

## Experience

**University Teaching Assistant** · Manara University · Nov 2025 – Sep 2026
- Taught 150+ students across the Robotics & Intelligent Systems, Mechatronics, and Informatics Engineering departments.
- Prepared lecture materials, lab exercises, and supplementary resources.
- Mentored two capstone groups of four students each in Mechatronics, from problem formulation to final delivery.
- Organized and supervised exams and quizzes, and graded them consistently and fairly.

---

## Skills

| | |
|---|---|
| **Languages** | Python, C/C++, MATLAB/Simulink, LaTeX, VHDL |
| **AI & Vision** | Deep learning, PyTorch, YOLOv8, feature extraction and matching (SuperPoint, DISK, LightGlue), HLOC, COLMAP, OpenMVS, signal processing |
| **Robotics & Control** | ROS, Gazebo, Arduino, Raspberry Pi, LQR, Lyapunov and adaptive control |
| **Tools** | Git/GitHub, CATIA V5 |
| **Human languages** | Arabic (native), English (C1) |

---

## Honours & Volunteering

- **ICPC regionals:** 3rd of 33 teams (Syrian Private Universities Collegiate Programming Contest) and 33rd of 89 teams (Syrian Collegiate Programming Contest)
- **Bronze Medal**, National WRO Future Engineers (2022)
- **Honorable Mention**, International Mathematical Modelling Challenge (2020)
- **Exhibitor**, Damascus International Fair, robotics project (2025)
- **Volunteer** cross-cultural and English conversation partner with Acquaint (2025–present) and ENGin (2025, 25.3 hours)

---

## Contact

I am happy to talk about research collaborations, internships, and projects in 3D vision, generative models, and autonomous systems.

[Bisher.Alsaleh@outlook.com](mailto:Bisher.Alsaleh@outlook.com) · [LinkedIn](https://www.linkedin.com/in/bisher-alsaleh)

<p align="center"><i>Advancing intelligent autonomy to preserve culture and enhance human life.</i></p>
