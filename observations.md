---
layout: page
title: Observations
permalink: /observations/
---

<style>
  .observations-grid {
    margin-top: 4px;
  }

  .observation-item {
    width: 220px !important;
    max-width: 100%;
    margin: 0 0 36px;
  }

  .observation-meta {
    margin: 0 0 8px;
    color: var(--muted);
    font-size: 13px;
    line-height: 1.4;
    white-space: nowrap;
  }

  .observation-thumb {
    display: block !important;
    width: 220px !important;
    max-width: 100% !important;
    margin: 0 !important;
    padding: 0 !important;
    border: 0 !important;
    background: transparent !important;
    cursor: zoom-in;
  }

  .observation-thumb img {
    display: block !important;
    width: 220px !important;
    max-width: 100% !important;
    height: auto !important;
    margin: 0 !important;
  }

  .observation-thumb:focus-visible {
    outline: 2px solid var(--text);
    outline-offset: 4px;
  }

  .observation-lightbox {
    position: fixed;
    width: auto;
    max-width: 82vw;
    max-height: 84vh;
    margin: auto;
    padding: 16px;
    overflow: visible;
    border: 0;
    border-radius: 2px;
    background: #fff;
    box-shadow: 0 18px 60px rgba(0,0,0,.35);
  }

  .observation-lightbox::backdrop {
    background: rgba(0,0,0,.78);
  }

  .lightbox-image {
    display: block !important;
    width: auto !important;
    height: auto !important;
    max-width: min(78vw, 900px) !important;
    max-height: calc(84vh - 32px) !important;
    margin: 0 auto !important;
    object-fit: contain;
  }

  .lightbox-close {
    position: absolute;
    top: -36px;
    right: 0;
    width: 30px;
    height: 30px;
    padding: 0;
    border: 0;
    background: transparent;
    color: #fff;
    font: inherit;
    font-size: 28px;
    line-height: 28px;
    cursor: pointer;
  }

  @media (max-width: 560px) {
    .observation-item,
    .observation-thumb,
    .observation-thumb img {
      width: 180px !important;
    }

    .observation-lightbox {
      max-width: 90vw;
      max-height: 82vh;
      padding: 10px;
    }

    .lightbox-image {
      max-width: calc(90vw - 20px) !important;
      max-height: calc(82vh - 20px) !important;
    }
  }
</style>

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
        width="220"
        height="165"
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
