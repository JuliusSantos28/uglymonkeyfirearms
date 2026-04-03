---
layout: layouts/base.njk
title: Home
description: Ugly Monkey Firearms — veteran-owned company providing a full spectrum of FFL services, custom builds, and laser engraving.
---

<section class="hero">
  <div class="hero__content">
    <img src="/images/logo.jpg" alt="Ugly Monkey Firearms logo" class="hero__logo">
    <h1 class="hero__title">Ugly Monkey<br>Firearms</h1>
    <p class="hero__tagline">Custom Builds. Precision Work. No Compromises.</p>
    <span class="hero__badge">Veteran-Owned &amp; Operated</span>
    <div class="hero__cta">
      <a href="/gallery/" class="btn btn--primary">View Our Work</a>
      <a href="/contact/" class="btn btn--secondary">Get in Touch</a>
    </div>
  </div>
</section>

<section class="intro">
  <h2>Full Spectrum FFL Services</h2>
  <p>Ugly Monkey Firearms is a veteran-owned company providing a full spectrum of FFL services. From custom firearm builds and Cerakote finishes to precision laser engraving. Every project is crafted with detail, care, and attention.</p>
  <p>Check out our <a href="/gallery/">gallery</a> to see recent work, or <a href="/contact/">reach out</a> to start your next project.</p>
</section>

<section class="feed">
  <div class="feed__header">
    <h2>Latest from the Shop</h2>
    <a href="/gallery/" class="btn btn--secondary">View All Work</a>
  </div>
  <div class="feed__grid">
    {%- for item in gallery | reverse %}
    {%- if loop.index <= 8 %}
    <a href="/gallery/" class="feed__item">
      <img src="/images/gallery/{{ item.file }}" alt="{{ item.caption }}" loading="lazy">
    </a>
    {%- endif %}
    {%- endfor %}
  </div>
  <div class="feed__footer">
    <a href="https://www.instagram.com/uglymonkeyfirearms/" target="_blank" rel="noopener noreferrer" class="btn btn--instagram">
      <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
      Follow @uglymonkeyfirearms
    </a>
  </div>
</section>
