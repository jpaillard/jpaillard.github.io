---
layout: page
permalink: /code/
title: code
description: Open-source software and research code.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

<div class="github-profile-section">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>
{% endif %}

{% if site.data.repositories.github_repos %}

<h2 class="repo-section-title">Repositories</h2>
<div class="repo-grid">
  {% for entry in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=entry.repo description=entry.description %}
  {% endfor %}
</div>
{% endif %}
