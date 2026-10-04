---
layout: page
title: Observations
permalink: /observations/
---

<div class="observations-grid">
  <article class="observation-item">
    <p class="observation-meta">Harlem, New York <span aria-hidden="true">·</span> October 2026</p>
    <button
      class="observation-thumb"
      type="button"
      data-lightbox-src="{{ '/assets/img/harlem-woman-2026.jpg' | relative_url }}"
      data-lightbox-alt="Sketch of a woman smoking a cigarette in Harlem"
      aria-label="Open drawing from Harlem, New York, October 2026"
    >
      <img
        src="{{ '/assets/img/harlem-woman-2026.jpg' | relative_url }}"
        alt="Sketch of a woman smoking a cigarette in Harlem"
        loading="lazy"
      >
    </button>
  </article>
</div>

<dialog class="observation-lightbox" id="observation-lightbox" aria-label="Expanded drawing">
  <button class="lightbox-close" type="button" aria-label="Close enlarged drawing">×</button>
  <img class="lightbox-image" src="" alt="">
</dialog>

<script>
  (function () {
    var dialog = document.getElementById("observation-lightbox");
    if (!dialog || typeof dialog.showModal !== "function") return;

    var image = dialog.querySelector(".lightbox-image");
    var closeButton = dialog.querySelector(".lightbox-close");

    document.querySelectorAll(".observation-thumb").forEach(function (button) {
      button.addEventListener("click", function () {
        image.src = button.dataset.lightboxSrc;
        image.alt = button.dataset.lightboxAlt || "Expanded drawing";
        dialog.showModal();
      });
    });

    closeButton.addEventListener("click", function () {
      dialog.close();
    });

    dialog.addEventListener("click", function (event) {
      if (event.target === dialog) dialog.close();
    });

    dialog.addEventListener("close", function () {
      image.src = "";
      image.alt = "";
    });
  })();
</script>
