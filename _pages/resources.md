---
layout: page
permalink: /resources/
title: Lab Resources
description: Facilities, equipment, and resources of the Networked Autonomous and Intelligent Learning (NAIL) Lab
nav: true
nav_order: 6
---

<style>
.facilities-container {
  max-width: 1200px;
  margin: 0 auto;
}

.facility-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: #f8f9fa;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.facility-section h2 {
  color: #2c3e50;
  border-bottom: 3px solid #3498db;
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
}

.equipment-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.equipment-card {
  background: white;
  border-radius: 8px;
  padding: 1.5rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.equipment-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.equipment-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 6px;
  margin-bottom: 1rem;
}

.equipment-title {
  font-size: 1.1rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.equipment-description {
  color: #666;
  font-size: 0.95rem;
  line-height: 1.4;
}

.specs-list {
  background: white;
  border-radius: 8px;
  padding: 1.5rem;
  margin-top: 1rem;
}

.specs-list ul {
  list-style-type: none;
  padding: 0;
}

.specs-list li {
  padding: 0.5rem 0;
  border-bottom: 1px solid #eee;
  display: flex;
  align-items: center;
}

.specs-list li:last-child {
  border-bottom: none;
}

.specs-list li:before {
  content: "🔧";
  margin-right: 0.5rem;
}

.lab-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.stat-card {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 1.5rem;
  border-radius: 8px;
  text-align: center;
}

.stat-number {
  font-size: 2rem;
  font-weight: bold;
  display: block;
}

.stat-label {
  font-size: 0.9rem;
  opacity: 0.9;
  margin-top: 0.5rem;
}

.arena-showcase {
  background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
  color: white;
  padding: 2rem;
  border-radius: 10px;
  margin-top: 2rem;
  text-align: center;
}

.arena-image {
  width: 100%;
  max-width: 800px;
  height: auto;
  border-radius: 8px;
  margin: 1rem auto;
  display: block;
}
</style>

<div class="facilities-container">

# Lab Resources & Facilities

The **Networked Autonomous and Intelligent Learning (NAIL) Lab** is equipped with state-of-the-art facilities and cutting-edge equipment to support advanced research in autonomous systems, robotics, and human-machine collaboration.

---

<div class="facility-section">
## 🤖 Multi-Robotic Platform

Our heterogeneous multi-robotic platform enables comprehensive research across ground, aerial, and legged robotics systems.

<div class="equipment-grid">
  <div class="equipment-card">
    <img src="/assets/img/facilities/seeker_drone.png" alt="ModalAI Seeker SLAM Drone" class="equipment-image">
    <div class="equipment-title">ModalAI Seeker SLAM Drone</div>
    <div class="equipment-description">Autonomous SLAM-capable drone with advanced navigation and mapping capabilities. We have three units for multi-drone coordination research.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/sentinel_drone.png" alt="ModalAI Sentinel 5G & AI Drone" class="equipment-image">
    <div class="equipment-title">ModalAI Sentinel 5G & AI Drone</div>
    <div class="equipment-description">VOXL2 AI & 5G development drone with advanced processing capabilities for edge AI applications and high-speed communication.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/rosbot_pro.jpeg" alt="ROSbot 2 Pro" class="equipment-image">
    <div class="equipment-title">ROSbot 2.0 Pro (3 units)</div>
    <div class="equipment-description">Autonomous ground robots with comprehensive sensor suites, perfect for formation control and multi-agent coordination experiments.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/jackal_robot.jpeg" alt="Jackal Robot" class="equipment-image">
    <div class="equipment-title">Jackal J100 Robot</div>
    <div class="equipment-description">Equipped with 3D LiDAR (Velodyne Puck VLP-16) and Intel RealSense D435 camera for advanced perception and navigation research.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/custom_drone.jpeg" alt="Custom Drone" class="equipment-image">
    <div class="equipment-title">Self-Assembled Custom Drone</div>
    <div class="equipment-description">AI-powered customized drone platform designed and built in-house for specialized research applications and rapid prototyping.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/unitree_go2.jpeg" alt="Unitree Go2" class="equipment-image">
    <div class="equipment-title">Unitree Go2 Quadruped Robot</div>
    <div class="equipment-description">Advanced four-legged robot for studying dynamic locomotion, balance control, and legged robotics in complex environments.</div>
  </div>
</div>

<div class="lab-stats">
  <div class="stat-card">
    <span class="stat-number">9</span>
    <span class="stat-label">Robotic Platforms</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">4</span>
    <span class="stat-label">Autonomous Drones</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">4</span>
    <span class="stat-label">Ground Robots</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">1</span>
    <span class="stat-label">Quadruped Robot</span>
  </div>
</div>

</div>

---

<div class="facility-section">
## 💻 Computing Resources & Development Kits

High-performance computing infrastructure and specialized development platforms support our research in AI, machine learning, and real-time control systems.

<div class="specs-list">
### Workstations & High-Performance Computing
<ul>
  <li><strong>Dell Precision 7920 Tower:</strong> Dual Intel Xeon Bronze 3206R CPU, Dual NVIDIA RTX A5500 GPU, 64 GB Memory, 2 TB NVMe</li>
  <li><strong>Dell Precision 5820 Tower:</strong> Intel Xeon W-2245 CPU, NVIDIA RTX A5000 GPU, 128 GB Memory, 2 TB NVMe</li>
  <li><strong>Aurora R16 Desktops (3 units):</strong> Intel Core i9 14900KF CPU, NVIDIA GeForce RTX 4090, 64 GB Memory, 2x2TB M.2 SSD</li>
  <li><strong>Aurora R16 Desktop:</strong> Intel Core i9 14900KF CPU, NVIDIA GeForce RTX 4060, 64 GB Memory, 1 TB NVMe SSD</li>
  <li><strong>Alienware m18 Laptop:</strong> Intel Core i7 13700HX CPU, NVIDIA GeForce RTX 4060, 64 GB Memory, 2TB M.2 SSD</li>
</ul>

### Edge Computing & Development Platforms
<ul>
  <li><strong>NVIDIA Jetson AGX Orin 64GB:</strong> High-performance edge AI development kit</li>
  <li><strong>NVIDIA Jetson Xavier NX:</strong> Compact AI computing platform</li>
  <li><strong>Jetson Nano Development Kit:</strong> Entry-level AI and robotics development</li>
  <li><strong>MAX78000/MAX78002 Evaluation Kits (3 units):</strong> Ultra-low-power AI microcontrollers</li>
  <li><strong>STM32F746NG Discovery Kits (3 units):</strong> ARM Cortex-M7 based development platforms</li>
</ul>
</div>

</div>

---

<div class="facility-section">
## 🔬 Advanced Sensors & Equipment

Specialized sensors, measurement systems, and fabrication equipment enable precise experimentation and rapid prototyping.

<div class="specs-list">
### Perception & Measurement Systems
<ul>
  <li><strong>OptiTrack Motion Capture System:</strong> 8 Flex13-Black-Long Pass cameras, 24×24×8 ft capture volume, tracks ~14 objects simultaneously</li>
  <li><strong>Intel RealSense D435i Cameras (2 units):</strong> RGB-D cameras with IMU for visual odometry</li>
  <li><strong>Livox Mid-360 LiDAR:</strong> 360° scanning with minimal detection range capabilities</li>
  <li><strong>Hokuyo UST-10LX:</strong> Scanning laser rangefinder for precise distance measurements</li>
</ul>

### Fabrication & Prototyping
<ul>
  <li><strong>Prusa MK4-kit 3D Printer:</strong> High-precision 3D printing with Satin Sheet and Enclosure</li>
  <li><strong>Electronics Workshop:</strong> Component libraries and assembly tools for custom hardware development</li>
</ul>
</div>

</div>

---

<div class="arena-showcase">
## 🏟️ Testing Arena & Lab Space

<img src="/assets/img/facilities/testing_arena.png" alt="Multi-robot Testing Arena" class="arena-image">

### Laboratory Specifications
- **Research Space:** 800 sq ft dedicated graduate student research area
- **Testing Arena:** 300 sq ft controlled experimental environment
- **Motion Capture Volume:** 24×24×8 feet with precision tracking
- **Multi-Robot Capacity:** Simultaneous experiments with up to 14 autonomous agents

Our indoor testing arena is equipped with the OptiTrack motion capture system, providing sub-millimeter precision tracking for multi-robot experiments. The controlled environment enables safe testing of formation control, swarm behaviors, and human-robot interaction scenarios.

</div>

---

## Research Capabilities

The NAIL Lab's comprehensive facilities enable cutting-edge research in:

- **🎯 Multi-Agent Systems:** Coordination and control of heterogeneous robot teams
- **🧠 Learning-Based Control:** AI-driven adaptive control systems with real-time implementation
- **🤝 Human-Autonomy Teaming:** Safe and effective human-robot collaboration
- **🛡️ Safety-Critical Systems:** Control barrier functions and formal verification methods
- **📡 Networked Control:** Communication-aware distributed control systems
- **🎮 Edge AI:** On-device machine learning for autonomous systems

---

*For more information about accessing lab resources or potential collaborations, please [contact us](/contact/).*

</div>