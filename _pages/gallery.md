---
layout: page
permalink: /gallery/
title: Photo Gallery
nav: false
nav_order: 8
---

<style>
.gallery-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.gallery-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: var(--global-card-bg-color);
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
}

.gallery-section h2 {
  color: var(--global-theme-color);
  border-bottom: 3px solid var(--global-theme-color);
  padding-bottom: 0.75rem;
  margin-bottom: 2rem;
  font-weight: 600;
}

.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

@media (max-width: 768px) {
  .photo-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}

.photo-card {
  background: var(--global-card-bg-color);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 1px solid var(--global-divider-color);
}

.photo-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.photo-card img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  display: block;
}

.photo-card .photo-caption {
  padding: 1rem;
  text-align: center;
}

.photo-card .photo-caption h4 {
  margin: 0;
  color: var(--global-text-color);
  font-size: 1rem;
  font-weight: 600;
}

.photo-card .photo-caption p {
  margin: 0.5rem 0 0 0;
  color: var(--global-text-color-light);
  font-size: 0.9rem;
}

/* Lightbox styles */
.lightbox {
  display: none;
  position: fixed;
  z-index: 9999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  cursor: pointer;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 8px;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 30px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}
</style>

<div class="gallery-container">

<div class="gallery-section">
<h2>ICRA 2025 - Atlanta, Georgia</h2>
<p>NAIL Lab members presented their research at the IEEE International Conference on Robotics and Automation (ICRA) 2025 in Atlanta, Georgia.</p>

<div class="photo-grid">
  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/icra2025.jpeg' | relative_url }}" alt="ICRA 2025 Conference" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>ICRA 2025 Conference</h4>
      <p>Lab members at ICRA 2025</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/icra_LLM.jpeg' | relative_url }}" alt="LLM Navigation Poster" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>LLM-Guided Navigation</h4>
      <p>Poster presentation on aerial robot navigation</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/icra_LLM1.jpeg' | relative_url }}" alt="LLM Navigation Discussion" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>Research Discussion</h4>
      <p>Discussing LLM-guided navigation research</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/icra_facet.jpeg' | relative_url }}" alt="FACETS Poster" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>FACETS Presentation</h4>
      <p>Efficient object detection research</p>
    </div>
  </div>
</div>
</div>

<div class="gallery-section">
<h2>Lab Group Events</h2>
<p>NAIL Lab celebrates achievements and milestones together through regular group gatherings.</p>

<div class="photo-grid">
  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/2025_fall.jpeg' | relative_url }}" alt="Fall 2025 Group Dinner" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>Fall 2025</h4>
      <p>End of semester celebration</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/2025_spring.jpeg' | relative_url }}" alt="Spring 2025 Group Dinner" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>Spring 2025</h4>
      <p>Group dinner gathering</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/2024_spring.jpeg' | relative_url }}" alt="Spring 2024 Group Dinner" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>Spring 2024</h4>
      <p>Semester celebration dinner</p>
    </div>
  </div>

  <div class="photo-card">
    <img src="{{ '/assets/img/gallery/2023_spring.jpeg' | relative_url }}" alt="Spring 2023 Group Dinner" onclick="openLightbox(this.src)" style="cursor: zoom-in;">
    <div class="photo-caption">
      <h4>Spring 2023</h4>
      <p>Lab group gathering</p>
    </div>
  </div>
</div>
</div>

</div>

<!-- Lightbox -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="Enlarged photo">
</div>

<script>
function openLightbox(src) {
  document.getElementById('lightbox-img').src = src;
  document.getElementById('lightbox').style.display = 'block';
  document.body.style.overflow = 'hidden';
}

function closeLightbox() {
  document.getElementById('lightbox').style.display = 'none';
  document.body.style.overflow = 'auto';
}

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    closeLightbox();
  }
});
</script>
