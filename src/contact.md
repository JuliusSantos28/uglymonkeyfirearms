---
layout: layouts/base.njk
title: Contact
description: Get in touch with Ugly Monkey Firearms for custom builds, quotes, and inquiries.
---

<section class="page-header">
  <h1>Contact Us</h1>
  <p>Have a project in mind? Send us a message and we'll get back to you.</p>
</section>

<section class="contact">
  <div class="contact__info">
    <h2>Get in Touch</h2>
    <ul class="contact__details">
      <li>
        <strong>Email</strong>
        <a href="mailto:info@uglymonkeyfirearms.com">info@uglymonkeyfirearms.com</a>
      </li>
      <li>
        <strong>Instagram</strong>
        <a href="https://www.instagram.com/uglymonkeyfirearms/" target="_blank" rel="noopener noreferrer">@uglymonkeyfirearms</a>
      </li>
    </ul>
  </div>

  <div class="contact__form-wrapper">
    <h2>Send us an email!</h2>
    <!-- Replace YOUR_FORM_ID with your Formspree form ID -->
    <form class="form" action="https://formspree.io/f/xpqojgnj" method="POST">
      <div class="form__group">
        <label class="form__label" for="name">Name</label>
        <input class="form__input" type="text" id="name" name="name" required>
      </div>
      <div class="form__group">
        <label class="form__label" for="email">Email</label>
        <input class="form__input" type="email" id="email" name="email" required>
      </div>
      <div class="form__group">
        <label class="form__label" for="message">Message</label>
        <textarea class="form__input form__textarea" id="message" name="message" rows="5" required></textarea>
      </div>
      <button class="btn btn--primary" type="submit">Send Message</button>
    </form>
  </div>
</section>
