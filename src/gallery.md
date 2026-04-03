---
layout: layouts/base.njk
title: Gallery
description: Browse recent custom firearm builds, laser engraving, and projects by Ugly Monkey Firearms.
---

<section class="page-header">
  <h1>Our Work</h1>
  <p>Custom builds, Cerakote finishes, stippling, laser engraving, and more.</p>
</section>

<section class="gallery">
  <div class="gallery__grid">
    {%- for item in gallery %}
    <a href="/images/gallery/{{ item.file }}" class="gallery__item" data-caption="{{ item.caption }}">
      <img src="/images/gallery/{{ item.file }}" alt="{{ item.caption }}" loading="lazy">
      <div class="gallery__overlay">
        <span class="gallery__caption">{{ item.caption }}</span>
      </div>
    </a>
    {%- endfor %}
  </div>
</section>

<div class="lightbox" id="lightbox" aria-hidden="true">
  <button class="lightbox__close" aria-label="Close">&times;</button>
  <button class="lightbox__prev" aria-label="Previous">&lsaquo;</button>
  <button class="lightbox__next" aria-label="Next">&rsaquo;</button>
  <img class="lightbox__img" src="" alt="">
  <p class="lightbox__caption"></p>
</div>

<script>
(function() {
  const items = document.querySelectorAll('.gallery__item');
  const lightbox = document.getElementById('lightbox');
  const lbImg = lightbox.querySelector('.lightbox__img');
  const lbCaption = lightbox.querySelector('.lightbox__caption');
  let current = 0;

  function open(i) {
    current = i;
    lbImg.src = items[i].href;
    lbCaption.textContent = items[i].dataset.caption;
    lightbox.classList.add('lightbox--open');
    document.body.style.overflow = 'hidden';
  }

  function close() {
    lightbox.classList.remove('lightbox--open');
    document.body.style.overflow = '';
  }

  function nav(dir) {
    current = (current + dir + items.length) % items.length;
    lbImg.src = items[current].href;
    lbCaption.textContent = items[current].dataset.caption;
  }

  items.forEach(function(item, i) {
    item.addEventListener('click', function(e) {
      e.preventDefault();
      open(i);
    });
  });

  lightbox.querySelector('.lightbox__close').addEventListener('click', close);
  lightbox.querySelector('.lightbox__prev').addEventListener('click', function() { nav(-1); });
  lightbox.querySelector('.lightbox__next').addEventListener('click', function() { nav(1); });
  lightbox.addEventListener('click', function(e) {
    if (e.target === lightbox) close();
  });
  document.addEventListener('keydown', function(e) {
    if (!lightbox.classList.contains('lightbox--open')) return;
    if (e.key === 'Escape') close();
    if (e.key === 'ArrowLeft') nav(-1);
    if (e.key === 'ArrowRight') nav(1);
  });
})();
</script>
