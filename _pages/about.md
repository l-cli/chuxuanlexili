---
layout: about
title: About
permalink: /
subtitle: <a href="#">University of Pennsylvania</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # disable default icon glyph bar

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

Staying on the wavefront of AI for better medicine.

<div class="intro-links" style="margin: 1.25rem 0 1.75rem 0; line-height: 1.85;">
  <div><strong>Curriculum Vitae:</strong> <a href="{{ '/assets/pdf/cv.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer">Download CV (PDF)</a></div>
  <div><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/chuxuan-li" target="_blank" rel="noopener noreferrer">https://www.linkedin.com/in/chuxuan-li</a></div>
  <div><strong>GitHub:</strong> <a href="https://github.com/l-cli" target="_blank" rel="noopener noreferrer">https://github.com/l-cli</a></div>
  <div><strong>Google Scholar:</strong> <a href="https://scholar.google.com/citations?user=6FHpDjAAAAAJ" target="_blank" rel="noopener noreferrer">https://scholar.google.com/citations?user=6FHpDjAAAAAJ</a></div>
</div>

<div id="contact-address">
  <h4>Department of Biostatistics, Epidemiology, and Informatics</h4>
  <p>3600 Civic Center Blvd</p>
  <p>Philadelphia, PA 19104</p>
  <p>Email: <a href="mailto:lexi.li@pennmedicine.upenn.edu">lexi.li@pennmedicine.upenn.edu</a></p>
</div>

<script>
(function() {
  function setupHomepageLayout() {
    // 1. Align profile photo to the exact same vertical height as the name header
    var header = document.querySelector(".post .post-header");
    var profile = document.querySelector(".post article .profile");
    if (header && profile && !document.getElementById("header-profile-row")) {
      var row = document.createElement("div");
      row.id = "header-profile-row";
      header.parentNode.insertBefore(row, header);

      var leftCol = document.createElement("div");
      leftCol.className = "header-profile-left";
      leftCol.appendChild(header);

      var rightCol = document.createElement("div");
      rightCol.className = "header-profile-right";
      rightCol.appendChild(profile);

      row.appendChild(leftCol);
      row.appendChild(rightCol);
    }

    // 2. Move address to the bottom of the page after Selected Publications
    var addr = document.getElementById("contact-address");
    var article = document.querySelector(".post article");
    if (addr && article) {
      article.appendChild(addr);
    }
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", setupHomepageLayout);
  } else {
    setupHomepageLayout();
  }
})();
</script>
