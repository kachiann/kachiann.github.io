---
layout: page
permalink: /repositories/
title: repositories
description: A selection of my open-source projects in data engineering, machine learning, and agentic AI.
nav: true
nav_order: 4
---

<!-- Intro for recruiters -->
<p>
  Below is a curated selection of my public repositories, organised by focus area. 
  Each project reflects production-minded engineering — documented, reproducible, 
  and built to demonstrate real-world data skills.
  Full profile at <a href="https://github.com/kachiann" target="_blank">github.com/kachiann</a>.
</p>

---

{% if site.data.repositories.github_users %}

## GitHub Profile

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
</div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## 🗄️ Data Engineering & Analytics

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% assign de_repos = "kachiann/immo-preisrechner-rlp_de,kachiann/Citi-Bike-Analytics-Pipeline,kachiann/nourishmama,kachiann/project-mlops" | split: "," %}
  {% for repo in de_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

---

## 🤖 Agentic AI & LLMs

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% assign ai_repos = "kachiann/maternal-health-ai-assistant,kachiann/agentic-data-analyst" | split: "," %}
  {% for repo in ai_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

---

## 📈 Data Science & Machine Learning

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% assign ds_repos = "kachiann/multi-asset-trend-forecaster,kachiann/financial-time-series-explorer,kachiann/Hotel_Booking_Cancellations" | split: "," %}
  {% for repo in ds_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

{% endif %}
