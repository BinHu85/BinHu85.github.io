---
layout: default
permalink: /team-members/
title: Team Members
description:
nav: false
nav_order: 4
---

<style>
  .member-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
    justify-items: center;
    align-items: stretch;
    max-width: 700px;
    margin: 0 auto;
  }
  @media (max-width: 768px) {
    .member-grid {
      grid-template-columns: 1fr;
      max-width: 320px;
      gap: 20px;
    }
  }
  .member-grid:has(.member-card:only-child) {
    justify-items: start;
  }
  .member-card {
    text-align: center;
    background: #f8f9fa;
    border-radius: 10px;
    padding: 18px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    width: 100%;
    max-width: 320px;
    min-height: 400px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .member-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
  }
  .member-photo {
    width: 160px;
    height: 160px;
    min-height: 160px;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid #dee2e6;
    background-color: #f8f9fa;
    transition: border-color 0.3s ease;
    margin: 0 auto 18px auto;
    display: block;
  }
  .member-card:hover .member-photo {
    border-color: #C8102E;
  }
  .member-name {
    font-size: 1.3em;
    font-weight: bold;
    margin-top: 8px;
    margin-bottom: 8px;
    color: #C8102E;
    line-height: 1.3;
  }
  .member-role {
    font-size: 0.95em;
    color: #666;
    margin-bottom: 15px;
    font-weight: 500;
  }
  .member-research {
    font-size: 1.0em;
    color: #007bff;
    font-weight: 500;
    background-color: #e3f2fd;
    padding: 8px 14px;
    border-radius: 18px;
    display: inline-block;
    margin: 10px 0;
    line-height: 1.3;
  }
  .member-interests {
    font-size: 0.9em;
    color: #666;
    font-style: italic;
    margin-top: auto;
    padding: 12px 15px;
    line-height: 1.5;
    flex-grow: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background-color: #f8f9fa;
    border-radius: 10px;
    margin-top: 15px;
  }
  .member-publications {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    justify-content: center;
    margin-top: 10px;
  }
  .pub-badge {
    display: inline-block;
    font-size: 0.75em;
    font-weight: 600;
    color: #fff;
    background: linear-gradient(135deg, #C8102E 0%, #8B0000 100%);
    padding: 4px 10px;
    border-radius: 12px;
    text-decoration: none;
    transition: all 0.3s ease;
    box-shadow: 0 2px 4px rgba(0,0,0,0.15);
  }
  .pub-badge:hover {
    background: linear-gradient(135deg, #A00D26 0%, #6B0000 100%);
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    color: #fff;
    text-decoration: none;
  }
  .member-card-content {
    display: flex;
    flex-direction: column;
    height: 100%;
    gap: 8px;
    justify-content: space-between;
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

  .lab-director-card {
    text-align: center;
    background: #f8f9fa;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    max-width: 280px;
    margin: 0 auto;
  }
  .lab-director-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
  }
  .lab-director-photo {
    width: 200px;
    height: 200px;
    min-height: 200px;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid #dee2e6;
    background-color: #f8f9fa;
    transition: border-color 0.3s ease;
    margin-bottom: 20px;
  }
  .lab-director-card:hover .lab-director-photo {
    border-color: #C8102E;
  }
  .lab-director-name {
    font-size: 1.4em;
    font-weight: bold;
    margin-bottom: 10px;
    color: #333;
  }
  .lab-director-name a {
    color: #C8102E;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  .lab-director-name a:hover {
    color: #A00D26;
    text-decoration: underline;
  }

  /* Custom carousel caption styling */
  .carousel-caption {
    position: absolute;
    bottom: 10px;
    right: 100px;
    left: auto;
    text-align: right;
    background: none;
    padding: 10px;
    transform: none;
    width: auto;
  }
  .carousel-caption h4,
  .carousel-caption p {
    color: white !important;
    text-shadow: 2px 2px 6px rgba(0,0,0,0.9);
    margin: 0;
    font-weight: bold;
    font-size: 1.7em;
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

<div class="lab-director-card">
  <a href="/">
    <img class="lab-director-photo" src="/assets/img/Hu_now.jpg" alt="Dr. Bin Hu">
  </a>
  <div class="lab-director-name"><a href="/">Dr. Bin Hu</a></div>
  <div class="member-role">PI & NAIL Lab Director</div>
</div>


---
##### **Ph.D. Students**
<div class="member-grid">
  {% assign members = site.data.phd_members %}
  {% for member in members %}
  <div class="member-card">
    <div class="member-card-content">
      {% if member.website %}
      <a href="{{ member.website }}" target="_blank" rel="noopener noreferrer">
        <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
      </a>
      {% else %}
      <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
      {% endif %}
      <div class="member-name">
        {{ member.name }}
        {% if member.website %}
        <a href="{{ member.website }}" target="_blank" rel="noopener noreferrer" style="margin-left: 8px; color: #007bff; text-decoration: none;">
          <i class="fas fa-globe" title="Visit personal website"></i>
        </a>
        {% endif %}
      </div>
      <div class="member-role">{{ member.role }}</div>
      {% if member.co_advisor %}
      <div class="member-role" style="font-size: 0.85em; color: #000;">
        {% if member.co_advisor_link %}
        <a href="{{ member.co_advisor_link }}" target="_blank" rel="noopener noreferrer" style="color: #000; text-decoration: none;">{{ member.co_advisor }}</a>
        {% else %}
        {{ member.co_advisor }}
        {% endif %}
      </div>
      {% endif %}
      <div class="member-research">{{ member.research }}</div>
      {% if member.publications %}
      <div class="member-publications">
        {% for pub in member.publications %}
        <a href="{{ pub.url }}" target="_blank" rel="noopener noreferrer" class="pub-badge">{{ pub.venue }}</a>
        {% endfor %}
      </div>
      {% endif %}
      {% if member.interests %}
      <div class="member-interests">{{ member.interests }}</div>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

---

##### **Master Students**

<div class="member-grid">
  {% assign members = site.data.master_members %}
  {% for member in members %}
  <div class="member-card">
    <div class="member-card-content">
      <img class="member-photo" src="{{ member.photo }}" alt="{{ member.name }}">
      <div class="member-name">{{ member.name }}</div>
      <div class="member-role">{{ member.role }}</div>
      <div class="member-research">{{ member.research }}</div>
      {% if member.publications %}
      <div class="member-publications">
        {% for pub in member.publications %}
        <a href="{{ pub.url }}" target="_blank" rel="noopener noreferrer" class="pub-badge">{{ pub.venue }}</a>
        {% endfor %}
      </div>
      {% endif %}
      {% if member.interests %}
      <div class="member-interests">{{ member.interests }}</div>
      {% endif %}
    </div>
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

##### **Previous Master Students**
- **Pooyan Ghodrati** (2025, M.S. Engineering Data Science, RA funded by NASA at UH, now Data Scientist at Toyo Financial Group)
- **Jahanvi Hitesh Dave** (2023, M.S. Computer Science, RA funded by NSF at UH, now at Goldman Sachs)

##### **Previous Undergraduate Students**
- **Victor Le** (2025, AI-powered Drone Project at UH)
- **Angel Gomez** (2025, AI-powered Drone Project at UH)
- **Hieu Le** (2025, AI-powered Drone Project at UH)
- **Nicolas Upshaw** (2025, AI-powered Drone Project at UH)
- **Yosef Abushaaban** (2025, AI-powered Race Car Project at UH)
- **Muhammad Ansari** (2025, AI-powered Race Car Project at UH)
- **Damian Castillo** (2025, AI-powered Race Car Project at UH)
- **Asaad Elsayed** (2025, AI-powered Race Car Project at UH)
- **Alejandro Zamarron** (2025, AI-powered Race Car Project at UH)
- **Javier Caudle** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Steven Comayagua** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Leandra Guzman** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Weijie Huang** (2024, Captone project-*Advance Surveillance Drone* at UH)
- **Edward Perez** (2024, Captone project-*Advance Surveillance Drone* at UH)
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
