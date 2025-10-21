---
layout: page
permalink: /demonstrations/
title: Demonstrations
nav: false
nav_order: 7
---

<style>
.demo-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.demo-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: var(--global-card-bg-color);
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
}

.demo-section h2 {
  color: var(--global-theme-color);
  border-bottom: 3px solid var(--global-theme-color);
  padding-bottom: 0.75rem;
  margin-bottom: 2rem;
  font-weight: 600;
}

.video-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .video-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}

.video-card {
  background: var(--global-card-bg-color);
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
  transition: all 0.3s ease;
}

.video-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.video-container {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
  height: 0;
  margin-bottom: 1.5rem;
  border-radius: 8px;
  overflow: hidden;
  background: var(--global-bg-color);
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
  border-radius: 8px;
}

.video-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--global-text-color);
  margin-bottom: 0.75rem;
  line-height: 1.3;
}

.video-description {
  color: var(--global-text-color-light);
  font-size: 0.95rem;
  line-height: 1.5;
}

.featured-video {
  grid-column: 1 / -1;
  max-width: 800px;
  justify-self: center;
}

.featured-video .video-container {
  padding-bottom: 45%; /* Slightly wider for featured */
}

@media (max-width: 768px) {
  .demo-container {
    padding: 0 0.5rem;
  }
  
  .demo-section {
    padding: 1.5rem;
    margin-bottom: 2rem;
  }
  
  .video-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="demo-container">

<p>The NAIL Lab focuses on developing resilient and sustainable intelligent networked autonomous systems. Our demonstrations showcase real-world applications of our research in multi-agent systems, learning-based control, human-autonomy teaming, and safety-critical systems.</p>

<hr>

<div class="demo-section">
<h2>📚 Research Projects & Publications</h2>

<p>Video demonstrations accompanying our published research papers and ongoing research projects.</p>

<div class="video-grid">
  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/-6Rd6V3HaoI" 
              title="Perception-Aware Leader-Follower Control with CBFs | ICRA 2025"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">Perception-Aware Leader-Follower Control with CBFs | ICRA 2025 (Expriment Video)</div>
    <div class="video-description">Two ROSbot Pro 2 robots demonstrate perception-aware leader-follower control using Control Barrier Functions (CBFs) to maintain visual contact. Our approach reliably keeps the leader within the follower's field of view, while conventional formation control without CBFs often loses visual contact, leading to unsafe behavior.</div>
  </div>

  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/3_sPaKcrOyE" 
              title="Distributed Leader-Follower Formation Control with Vision Constraints | ICRA 2025 Submission"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">Distributed Leader-Follower Formation Control with Vision Constraints | ICRA 2025 (Supplementary Video)</div>
    <div class="video-description">A perception-aware distributed formation control scheme for agents using body-fixed cameras with limited field of view (FOV). Our CBF-based approach ensures leader visibility by incorporating FOV constraints, while neural network and double bounding box estimators provide robust state estimation from real-time image data across various environments.</div>
  </div>

  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/jgrmN9YZ8vA" 
              title="FACETS: Efficient Once-for-all Object Detection via Constrained Iterative Search | ICRA 2025"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">FACETS: Efficient Once-for-all Object Detection via Constrained Iterative Search | ICRA 2025 (Late Breaking Session)</div>
    <div class="video-description">Our FACETS-derived model running on the MAX78000 microcontroller demonstrates efficient object detection within tight hardware constraints (432 KB memory, 32-layer limit). Despite these limitations, it achieves 45.4% less energy consumption, 29.3% lower latency, and 4.5% higher mAP compared to Analog Devices' TinierSSD baseline.</div>
  </div>

  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/uHh0LyTN1c0" 
              title="Toward Embedded LLM-Guided Navigation and Object Detection for Aerial Robots | ICRA 2025"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">Toward Embedded LLM-Guided Navigation and Object Detection for Aerial Robots | ICRA 2025 (Late Breaking Session)</div>
    <div class="video-description">A hierarchical framework integrating natural language commands with autonomous quadrotor navigation using the ModalAI Seeker drone. Our fine-tuned LLaMA model (via LoRA) interprets high-level instructions into task goals, while the drone executes them through onboard VIO-based control, path planning, and real-time object detection with hardware-in-the-loop testing.</div>
  </div>
</div>

</div>

<hr>

<div class="demo-section">
<h2>🎓 Capstone Research Projects</h2>

<p>Undergraduate and graduate student project demonstrations showcasing innovative applications and learning outcomes.</p>

<div class="video-grid">
  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/fM09gTBHnnM" 
              title="UH Students Build Autonomous Drone with Real-Time Object Detection | NAIL Lab Capstone Project"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">UH Students Build Autonomous Drone with Real-Time Object Detection | NAIL Lab Capstone Project</div>
    <div class="video-description">Computer Engineering Technology undergraduates designed, assembled, and programmed this custom drone from scratch as their senior capstone project. Working under NAIL Lab guidance, the drone features autonomous navigation using OptiTrack motion capture and real-time onboard object detection—demonstrating hands-on robotics and AI development by UH students.</div>
  </div>
</div>

</div>

<hr>

<div class="demo-section">
<h2>🔬 Lab Equipment Demonstrations</h2>

<p>Demonstrations showcasing our AI-driven heterogenous robotic platforms and their autonomous capabilities in real-world scenarios.</p>

<div class="video-grid">
  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/lwVmqo9jDYw"  
              title="Autonomous UAV Landing on Moving UGV | Multi-Robot Collaboration by NAIL Lab UH"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">Autonomous UAV Landing on Moving UGV | Multi-Robot Collaboration</div>
    <div class="video-description">Demonstration of advanced multi-robot coordination where an autonomous UAV successfully lands on a moving ground vehicle, showcasing precise real-time control and inter-robot communication.</div>
  </div>

  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/rmnrWfe9tx8"  
              title="ModalAI Seeker SLAM Drone Demo: Mapping, Motion Planning & Object Detection"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">ModalAI Seeker SLAM Drone Demo: Mapping, Motion Planning & Object Detection</div>
    <div class="video-description">Live demonstration of our ModalAI Seeker drone performing simultaneous localization and mapping (SLAM), autonomous motion planning, and real-time object detection in complex environments.</div>
  </div>

  <div class="video-card">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/U8blNoet9O4"  
              title="Fully Autonomous Jackal Robot Demo | SLAM, Obstacle Avoidance & Object Detection | NAIL Lab UH"
              allowfullscreen>
      </iframe>
    </div>
    <div class="video-title">Fully Autonomous Jackal Robot Demo | SLAM, Obstacle Avoidance & Object Detection</div>
    <div class="video-description">Complete autonomous navigation demonstration featuring our Jackal robot performing SLAM, dynamic obstacle avoidance, and object detection in both indoor and outdoor environments.</div>
  </div>
</div>

</div>

<hr>

<p><em>For more information about our research capabilities or potential collaborations, please <a href="mailto:bhu12@uh.edu">contact us</a>.</em></p>

</div>