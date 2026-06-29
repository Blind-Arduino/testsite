---
layout: default
title: "Contact"
permalink: /contact/
description: "Contact the Blind Arduino Project."
---

## Get in Touch

We would love to hear from you! Use the form below to send us a message. We'll get back to you as soon as we can.

<div data-fs-success role="alert" tabindex="-1" id="contact-success">
<p>Your message has been sent. We'll get back to you soon!</p>
</div>

<div data-fs-error role="alert"></div>

<form id="contact-form" action="https://formspree.io/f/mojolvbd" method="POST" aria-label="Contact Blind Arduino">

  <div class="form-field">
    <label for="name">Your name <span aria-hidden="true">*</span></label>
    <input type="text" id="name" name="name" required aria-required="true" autocomplete="name" data-fs-field>
    <span data-fs-error="name"></span>
  </div>

  <div class="form-field">
    <label for="email">Your email address <span aria-hidden="true">*</span></label>
    <input type="email" id="email" name="email" required aria-required="true" autocomplete="email" data-fs-field>
    <span data-fs-error="email"></span>
  </div>

  <div class="form-field">
    <label for="topic">Topic <span aria-hidden="true">*</span></label>
    <select id="topic" name="topic" required aria-required="true" data-fs-field>
      <option value="">— Please select —</option>
      <option value="technical-question">Technical question</option>
      <option value="workshop-proposal">Workshop proposal</option>
      <option value="volunteer-inquiry">Volunteer inquiry</option>
      <option value="something-else">Something else</option>
    </select>
    <span data-fs-error="topic"></span>
  </div>

  <div class="form-field">
    <label for="message">Message <span aria-hidden="true">*</span></label>
    <textarea id="message" name="message" rows="6" required aria-required="true" data-fs-field></textarea>
    <span data-fs-error="message"></span>
  </div>

  <div>
    <button type="submit" data-fs-submit-btn>Send message</button>
  </div>

</form>

<script>
  window.formspree = window.formspree || function () { (formspree.q = formspree.q || []).push(arguments); };
  formspree('initForm', { formElement: '#contact-form', formId: 'mojolvbd' });

  document.addEventListener('DOMContentLoaded', function () {
    var success = document.getElementById('contact-success');
    if (!success) return;
    new MutationObserver(function () {
      if (success.offsetParent !== null) success.focus();
    }).observe(success, { attributes: true, attributeFilter: ['style', 'class'] });
  });
</script>
<script src="https://unpkg.com/@formspree/ajax@1" defer></script>
