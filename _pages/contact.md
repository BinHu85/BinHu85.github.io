---
layout: page
permalink: /contact/
title: Contact
nav: true
nav_order: 7
---

<style>
.contact-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 1rem;
}

.contact-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: var(--global-card-bg-color);
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid var(--global-divider-color);
}

.contact-section h2 {
  color: var(--global-theme-color);
  border-bottom: 3px solid var(--global-theme-color);
  padding-bottom: 0.75rem;
  margin-bottom: 2rem;
  font-weight: 600;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: start;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1rem;
  background: var(--global-bg-color);
  border-radius: 8px;
  border: 1px solid var(--global-divider-color);
}

.contact-icon {
  font-size: 1.2rem;
  color: var(--global-theme-color);
  margin-top: 0.2rem;
  min-width: 1.5rem;
}

.contact-details h3 {
  margin: 0 0 0.5rem 0;
  color: var(--global-text-color);
  font-size: 1.1rem;
  font-weight: 600;
}

.contact-details p {
  margin: 0;
  color: var(--global-text-color-light);
  line-height: 1.5;
}

.contact-details a {
  color: var(--global-theme-color);
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-details a:hover {
  color: var(--global-hover-color);
  text-decoration: underline;
}

.image-row {
  text-align: center;
  margin-bottom: 2rem;
}

.location-image {
  width: 100%;
  max-width: 800px;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 10px 25px -3px rgba(0, 0, 0, 0.2);
  margin: 0 auto;
  display: block;
}

.map-container {
  margin-top: 2rem;
}

.map-embed {
  width: 100%;
  height: 400px;
  border: 0;
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .map-embed {
    height: 300px;
  }
}

</style>

<div class="contact-container">

<div class="contact-section">
<h2>📍 Lab Location & Contact Information</h2>

<!-- First Row: Image takes full width -->
<div class="image-row">
  <img src="/assets/img/sugarland_location.jpg" alt="NAIL Lab at UH Sugar Land" class="location-image">
  <p style="text-align: center; color: var(--global-text-color-light); font-style: italic; margin-top: 1rem;">
    Engineering Building 4 (SAB2) on the left and Engineering Building 3 (SAB1) on the right at University of Houston Sugar Land Campus
  </p>
</div>

<!-- Second Row: Two columns for contact and address -->
<div class="contact-grid">
  <div class="contact-item">
    <div class="contact-icon">
      <i class="fas fa-user"></i>
    </div>
    <div class="contact-details">
      <h3>NAIL Lab Director</h3>
      <p><strong>Dr. Bin Hu</strong><br>
      <a href="mailto:bhu12@uh.edu">bhu12@uh.edu</a><br>
      Department of Engineering Technology<br>
      University of Houston</p>
    </div>
  </div>

  <div class="contact-item">
    <div class="contact-icon">
      <i class="fas fa-map-marker-alt"></i>
    </div>
    <div class="contact-details">
      <h3>NAIL Lab Address</h3>
      <p>Engineering Building 4 (SAB2), Room 122<br>
      University of Houston Sugar Land<br>
      13850 University Blvd<br>
      Sugar Land, TX 77479</p>
    </div>
  </div>
</div>

</div>

<div class="contact-section">
<h2>🗺️ Find Us</h2>

<p>The NAIL Lab is located at the University of Houston Sugar Land campus, providing cutting-edge research facilities for AI-driven robotics and networked autonomous intelligent learning systems.</p>

<div class="map-container">
  <iframe
    class="map-embed"
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3464.8!2d-95.6342!3d29.6212!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x864076b5c5f0f0f1%3A0x8b8b8b8b8b8b8b8b!2s13850%20University%20Blvd%2C%20Sugar%20Land%2C%20TX%2077479!5e0!3m2!1sen!2sus!4v1699999999999!5m2!1sen!2sus"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>
</div>

<p style="margin-top: 1rem; text-align: center;">
  <a href="https://goo.gl/maps/UHSugarLand" target="_blank" rel="noopener noreferrer" style="color: var(--global-theme-color); text-decoration: none;">
    <i class="fas fa-external-link-alt"></i> View on Google Maps
  </a>
</p>

</div>


</div>