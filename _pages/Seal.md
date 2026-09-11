---
layout: default
title: Welcome Fellow Snakes 
permalink: /sealandserpent/
---

<form id="password-gate" style="text-align: center;">
  <button type="submit" aria-label="Enter password">
    <img src="{{ '/assets/images/crest.png' | relative_url }}" alt="Enter password" style="width: 100px; height: auto;">
  </button>
  <input id="page-password" name="password" type="password" required autofocus style="display: block; margin: 8px auto 0;">
  <p id="password-error" role="alert" hidden>Incorrect password.</p>
</form>

<div id="protected-content" hidden>
  <h2>Sealandserpent</h2>
  <p>hi</p>

</div>

<noscript>
  <p>This page requires JavaScript to verify the password.</p>
</noscript>

<script>
  (function () {
    const passwordGate = document.getElementById('password-gate');
    const passwordInput = document.getElementById('page-password');
    const passwordError = document.getElementById('password-error');
    const protectedContent = document.getElementById('protected-content');

    passwordGate.addEventListener('submit', function (event) {
      event.preventDefault();

      if (passwordInput.value === 'dvagasarpa') {
        passwordGate.hidden = true;
      protectedContent.hidden = false;
        return;
      }

      passwordError.hidden = false;
      passwordInput.select();
    });
  }());
</script>