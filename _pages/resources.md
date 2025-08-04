---
layout: page
permalink: /resources/
title: Lab Resources
nav: false
nav_order: 6
---

<style>
.facilities-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.facility-section {
  margin-bottom: 2.5rem;
  padding: 2rem;
  background: var(--global-card-bg-color);
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
}

.facility-section h2 {
  color: var(--global-theme-color);
  border-bottom: 3px solid var(--global-theme-color);
  padding-bottom: 0.75rem;
  margin-bottom: 2rem;
  font-weight: 600;
}

.equipment-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .equipment-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}

.equipment-card {
  background: var(--global-card-bg-color);
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
  transition: all 0.3s ease;
  height: fit-content;
}

.equipment-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.equipment-image {
  width: 100%;
  height: 200px;
  object-fit: contain;
  object-position: center;
  border-radius: 8px;
  margin-bottom: 1.25rem;
  background: var(--global-bg-color);
  border: 1px solid var(--global-divider-color);
}

.equipment-title {
  font-size: 1.2rem;
  font-weight: 600;
  color: var(--global-text-color);
  margin-bottom: 0.75rem;
  line-height: 1.3;
}

.equipment-description {
  color: var(--global-text-color-light);
  font-size: 0.95rem;
  line-height: 1.5;
}

.specs-list {
  background: var(--global-card-bg-color);
  border-radius: 12px;
  padding: 2rem;
  margin-top: 1.5rem;
  border: 1px solid var(--global-divider-color);
}

.specs-list h3 {
  color: var(--global-text-color);
  margin-bottom: 1.5rem;
  font-weight: 600;
}

.specs-list ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.specs-list li {
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--global-divider-color);
  display: flex;
  align-items: flex-start;
  color: var(--global-text-color);
}

.specs-list li:last-child {
  border-bottom: none;
}

.specs-list li:before {
  content: "🔧";
  margin-right: 0.75rem;
  margin-top: 0.1rem;
  flex-shrink: 0;
}

.lab-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .lab-stats {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
}

.stat-card {
  background: linear-gradient(135deg, var(--global-theme-color) 0%, var(--global-hover-color) 100%);
  color: white;
  padding: 2rem 1.5rem;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  display: block;
  line-height: 1;
}

.stat-label {
  font-size: 0.9rem;
  opacity: 0.95;
  margin-top: 0.5rem;
  font-weight: 500;
}

.arena-showcase {
  background: var(--global-card-bg-color);
  color: var(--global-text-color);
  padding: 3rem 2rem;
  border-radius: 16px;
  margin-top: 3rem;
  text-align: left;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
}

.arena-showcase h2 {
  color: var(--global-theme-color) !important;
  border-bottom: 3px solid var(--global-theme-color);
  margin-bottom: 2rem;
}

.arena-image {
  width: 100%;
  max-width: 800px;
  height: auto;
  border-radius: 12px;
  margin: 2rem 0;
  display: block;
  box-shadow: 0 10px 25px -3px rgba(0, 0, 0, 0.2);
}

@media (max-width: 768px) {
  .facilities-container {
    padding: 0 0.5rem;
  }
  
  .facility-section {
    padding: 1.5rem;
    margin-bottom: 2rem;
  }
  
  .arena-showcase {
    padding: 2rem 1.5rem;
  }
}
</style>

<div class="facilities-container">

<div class="facility-section">
<h2>🤖 Multi-Robotic Platform</h2>

<p>Our heterogeneous multi-robotic platform enables comprehensive research across ground, aerial, and legged robotics systems.</p>

<div class="equipment-grid">
  <div class="equipment-card">
    <img src="/assets/img/facilities/seeker_drone.png" alt="ModalAI Seeker SLAM Drone" class="equipment-image">
    <div class="equipment-title">ModalAI Seeker SLAM Drone (3 units)</div>
    <div class="equipment-description">Autonomous SLAM-capable drones with advanced navigation and mapping capabilities for multi-drone coordination research and swarm experiments.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/sentinel_drone.png" alt="ModalAI Sentinel 5G & AI Drone" class="equipment-image">
    <div class="equipment-title">ModalAI Sentinel 5G &amp; AI Drone</div>
    <div class="equipment-description">VOXL2 AI &amp; 5G development drone with advanced processing capabilities for edge AI applications and high-speed communication.</div>
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

</div>

<hr>

<div class="facility-section">
<h2>💻 Edge Computing &amp; Development Platforms</h2>

<p>Specialized development platforms and edge computing systems for AI, machine learning, and real-time embedded applications.</p>

<div class="equipment-grid">
  <div class="equipment-card">
    <img src="/assets/img/facilities/jetson_orin.jpg" alt="NVIDIA Jetson AGX Orin" class="equipment-image">
    <div class="equipment-title">NVIDIA Jetson AGX Orin 64GB</div>
    <div class="equipment-description">High-performance edge AI development kit with 275 TOPS of AI performance for advanced autonomous systems and robotics applications.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/jetson_xavier.jpg" alt="NVIDIA Jetson Xavier NX" class="equipment-image">
    <div class="equipment-title">NVIDIA Jetson Xavier NX</div>
    <div class="equipment-description">Compact AI computing platform delivering 21 TOPS of accelerated computing in a small form factor for edge AI applications.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/jetson_nano.jpg" alt="Jetson Nano Development Kit" class="equipment-image">
    <div class="equipment-title">Jetson Nano Development Kit</div>
    <div class="equipment-description">Entry-level AI and robotics development platform perfect for learning, prototyping, and deploying AI applications at the edge.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/max78000.jpg" alt="MAX78000 Evaluation Kit" class="equipment-image">
    <div class="equipment-title">MAX78000/MAX78002 Evaluation Kits (3 units)</div>
    <div class="equipment-description">Ultra-low-power AI microcontrollers with hardware-accelerated neural network processing for battery-powered edge AI applications.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/stm32f746.jpg" alt="STM32F746NG Discovery Kit" class="equipment-image">
    <div class="equipment-title">STM32F746NG Discovery Kits (3 units)</div>
    <div class="equipment-description">ARM Cortex-M7 based development platforms with touchscreen, Ethernet, and rich peripheral set for embedded systems development.</div>
  </div>
</div>

</div>

<hr>

<div class="facility-section">
<h2>🔬 Advanced Sensors &amp; Equipment</h2>

<p>Specialized sensors, measurement systems, and fabrication equipment enable precise experimentation and rapid prototyping.</p>

<div class="equipment-grid">
  <div class="equipment-card">
    <img src="/assets/img/facilities/optitrack.jpg" alt="OptiTrack Motion Capture System" class="equipment-image">
    <div class="equipment-title">OptiTrack Motion Capture System</div>
    <div class="equipment-description">8 Flex13-Black-Long Pass cameras with 24×24×8 ft capture volume, providing sub-millimeter precision tracking for up to 14 objects simultaneously.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/realsense_d435i.jpg" alt="Intel RealSense D435i" class="equipment-image">
    <div class="equipment-title">Intel RealSense D435i Cameras (2 units)</div>
    <div class="equipment-description">RGB-D cameras with integrated IMU for visual odometry, depth sensing, and 3D perception in robotics applications.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/livox_mid360.jpg" alt="Livox Mid-360 LiDAR" class="equipment-image">
    <div class="equipment-title">Livox Mid-360 LiDAR</div>
    <div class="equipment-description">360° scanning LiDAR with minimal detection range capabilities for high-resolution point cloud generation and mapping.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/hokuyo_ust10lx.jpg" alt="Hokuyo UST-10LX" class="equipment-image">
    <div class="equipment-title">Hokuyo UST-10LX</div>
    <div class="equipment-description">Scanning laser rangefinder providing precise distance measurements with high accuracy for robotics navigation and mapping.</div>
  </div>

  <div class="equipment-card">
    <img src="/assets/img/facilities/prusa_mk4.jpg" alt="Prusa MK4-kit 3D Printer" class="equipment-image">
    <div class="equipment-title">Prusa MK4-kit 3D Printer</div>
    <div class="equipment-description">High-precision 3D printing with Satin Sheet and Enclosure for rapid prototyping and custom component fabrication.</div>
  </div>
</div>

</div>

<hr>

<div class="arena-showcase">
<h2>🏟️ Testing Arena &amp; Lab Space</h2>

<img src="/assets/img/facilities/testing_arena.png" alt="Multi-robot Testing Arena" class="arena-image">

<h3>Laboratory Specifications</h3>
<div class="specs-list">
<ul>
<li><strong>Research Space:</strong> 800 sq ft dedicated graduate student research area | <strong>Testing Arena:</strong> 300 sq ft controlled experimental environment</li>
<li><strong>Motion Capture Volume:</strong> 24×24×8 feet with precision tracking | <strong>Multi-Robot Capacity:</strong> Up to 14 autonomous agents</li>
</ul>
</div>

<p>Our indoor testing arena is equipped with the OptiTrack motion capture system, providing sub-millimeter precision tracking for multi-robot experiments. The controlled environment enables safe testing of formation control, swarm behaviors, and human-robot interaction scenarios.</p>

</div>

<hr>

<h2>Research Capabilities</h2>

<p>The NAIL Lab's comprehensive facilities enable cutting-edge research in:</p>

<ul>
<li><strong>🎯 Multi-Agent Systems:</strong> Coordination and control of heterogeneous robot teams</li>
<li><strong>🧠 Learning-Based Control:</strong> AI-driven adaptive control systems with real-time implementation</li>
<li><strong>🤝 Human-Autonomy Teaming:</strong> Safe and effective human-robot collaboration</li>
<li><strong>🛡️ Safety-Critical Systems:</strong> Control barrier functions and formal verification methods</li>
<li><strong>📡 Networked Control:</strong> Communication-aware distributed control systems</li>
<li><strong>🎮 Edge AI:</strong> On-device machine learning for autonomous systems</li>
</ul>

<hr>

<p><em>For more information about accessing lab resources or potential collaborations, please <a href="mailto:bhu12@uh.edu">contact us</a>.</em></p>

</div>