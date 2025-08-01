---
layout: default
permalink: /lab/
title: NAIL Lab
description:
nav: true
nav_order: 4
---

<style>
  .member-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    justify-items: center;
    align-items: start;
  }
  .member-card {
    text-align: center;
    background: #f8f9fa;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .member-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
  }
  .member-photo {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid #dee2e6;
    transition: border-color 0.3s ease;
  }
  .member-card:hover .member-photo {
    border-color: #007bff;
  }
  .member-name {
    font-size: 1.2em;
    font-weight: bold;
    margin-top: 15px;
    margin-bottom: 8px;
    color: #333;
  }
  .member-role {
    font-size: 0.9em;
    color: #666;
    margin-bottom: 10px;
  }
  .member-research {
    font-size: 0.95em;
    color: #007bff;
    font-weight: 500;
    background-color: #e3f2fd;
    padding: 8px 12px;
    border-radius: 20px;
    display: inline-block;
    margin-top: 5px;
  }
  .member-interests {
    font-size: 0.85em;
    color: #666;
    font-style: italic;
    margin-top: 8px;
    padding: 0 10px;
    line-height: 1.4;
  }
  .funding-logos {
    text-align: center;
    background-color: #f9f9f9;
    padding: 1px 0;
    border-top: 1px solid #ddd;
    margin-top: 1px;
  }
  .funding-logos img {
    max-height: 100px;
    max-width: 140px;
    margin: 10px;
    object-fit: contain;
    transition: transform 0.3s ease;
  }
  .funding-logos img:hover {
    transform: scale(1.1);
  }

  @media (max-width: 768px) {
    .funding-logos img {
      max-height: 60px;
      max-width: 100px;
    }
  }
</style>


## Networked Autonomous Intelligent Learning (NAIL)
---
<div id="myCarousel" class="carousel slide" data-ride="carousel">
  <!-- Indicators -->
  <ol class="carousel-indicators">
    {% assign slides = site.data.slides %}
    {% for slide in slides %}
    <li data-target="#myCarousel" data-slide-to="{{ forloop.index0 }}" class="{% if forloop.first %}active{% endif %}"></li>
    {% endfor %}
  </ol>

  <!-- Wrapper for slides -->
  <div class="carousel-inner">
    {% for slide in slides %}
    <div class="carousel-item {% if forloop.first %}active{% endif %}">
      {% if slide.type == "image" %}
      <img src="{{ slide.url }}" class="d-block w-100 carousel-image" alt="{{ slide.alt_text }}">
      {% elsif slide.type == "video" %}
      <video class="d-block w-100 carousel-video" autoplay loop muted>
        <source src="{{ slide.url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      {% endif %}
      <div class="carousel-caption">
        <h4>{{ slide.title }}</h4>
        <p>{{ slide.description }}</p>
      </div>
    </div>
    {% endfor %}
  </div>

  <!-- Controls -->
  <a class="carousel-control-prev" href="#myCarousel" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#myCarousel" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
---
Welecome to NAIL Lab! The lab's goal is to develop resilient and sustainable intelligent networked autonomous systems capable of operating in highly dynamic, uncertain, and adversarial environments. The lab integrates expertise in **machine learning**, **control and optimization**, **wireless communication**, and **human factors** to design advanced algorithms and practical testbeds for **cyber-physical systems**, **human-AI autonomy**, and the **Internet of Things (IoT)**. 

- **Vehicular Networked Control Systems**
- **Embodied AI**
- **Autonomous Robotic Systems**
- **Smart Manufacturing Automation**
- **Networked Power Systems and Smart Grids**

---

### Current Team Members

##### **Lab Director**
-[Dr. Bin Hu](https://binhu85.github.io/)


---
##### **Ph.D. Students**
<div class="member-grid">
  {% assign members = site.data.phd_members %}
  {% for member in members %}
  <div class="member-card">
    <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
    <div class="member-name">{{ member.name }}</div>
    <div class="member-role">{{ member.role }}</div>
    <div class="member-research">{{ member.research }}</div>
    {% if member.interests %}
    <div class="member-interests">{{ member.interests }}</div>
    {% endif %}
  </div>
  {% endfor %}
</div>

---

##### **Master Students and Research Assistants**

<div class="member-grid">
  {% assign members = site.data.master_members %}
  {% for member in members %}
  <div class="member-card">
    <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
    <div class="member-name">{{ member.name }}</div>
    <div class="member-role">{{ member.role }}</div>
    <div class="member-research">{{ member.research }}</div>
    {% if member.interests %}
    <div class="member-interests">{{ member.interests }}</div>
    {% endif %}
  </div>
  {% endfor %}
</div>

---

##### **Undergraduate Students**

<div class="member-grid">
  {% assign members = site.data.undergrad_members %}
  {% for member in members %}
  <div class="member-card">
    <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
    <div class="member-name">{{ member.name }}</div>
    <div class="member-role">{{ member.role }}</div>
    <div class="member-research">{{ member.research }}</div>
    {% if member.interests %}
    <div class="member-interests">{{ member.interests }}</div>
    {% endif %}
  </div>
  {% endfor %}
</div>
---

### Alumni
##### **Previous Undergraduate Students, Master Students and Research Assistants**
- **Javier Caudle** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Steven Comayagua** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Leandra Guzman** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Weijie Huang** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Edward Perez** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Jahanvi Hitesh Dave** (2023, RA funded by NSF at UH, now at Goldman Sachs)
- **Kristof Siska** (2019–2022, RA funded by NSF, now Master's student at Old Dominion University)  
- **Jacob Michalick** (2022, RA funded by DoD at ODU)  
- **Skye Taylor** (2021, RA funded by NSF REU, now Master's student at University of Virginia)  
- **Joshua Smith** (2021, RA funded by NSF at ODU)  
- **Andrew Vecerkauskas** (2020, RA funded by ONR at ODU)  
- **Jeremy Sklute** (2020)  
- **Teresa Trinh** (2019, RA funded by ONR  at ODU)  
- **Zachariah Garvin** (2019, RA funded by ONR at ODU)  
- **Thomas Sexton** (2019, RA funded by ONR at ODU)  
- **Bryan Holland** (2019, RA funded by ONR at ODU)  
- **Matthew Kersey** (2019, RA funded by ONR at ODU)  
- **Victor Ortiz** (2018)

---

### Join Us
We are always looking for talented and motivated individuals passionate about cutting-edge research in intelligent and networked autonomous systems. If you're interested, please contact **Dr. Bin Hu** for opportunities.

---

### Acknowledgment
We gratefully acknowledge the support from our funding agencies, including the National Science Foundation (NSF), the National Aeronautics and Space Administration (NASA), and the Office of Naval Research (ONR), for enabling our research in intelligent and networked autonomous systems.
<div class="funding-logos">
  <img src="/assets/img/nsf-logo.jfif" alt="NSF Logo">
  <img src="/assets/img/nasa-logo.png" alt="NASA Logo">
  <img src="/assets/img/onr-logo.png" alt="ONR Logo">
</div>
