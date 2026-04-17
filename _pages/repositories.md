---
layout: page
permalink: /code/
title: code
description:
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% endif %}

{% if site.data.repositories.github_repos %}

## Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for entry in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=entry.repo description=entry.description %}
  {% endfor %}
</div>
{% endif %}
