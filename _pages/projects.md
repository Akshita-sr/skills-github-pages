---
title: "My Projects"
permalink: /projects/
layout: collection
collection: portfolio
entries_layout: grid
classes: wide
author_profile: true
header:
  overlay_image: /assets/images/projects-header.jpg
  overlay_filter: 0.5
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "A showcase of my professional and personal projects."
---

## Featured Projects

Below are some of my featured projects. Each project includes details about the technologies used, my role, and the outcomes achieved.

{% for project in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}

## GitHub Repositories

In addition to the featured projects above, you can explore my other projects on GitHub.

<div class="entries-{{ entries_layout }}">
  {% for repository in site.github.public_repositories %}
    {% if repository.fork == false %}
      <div class="grid__item">
        <article class="archive__item">
          <h2 class="archive__item-title">
            <a href="{{ repository.html_url }}" target="_blank">{{ repository.name }}</a>
          </h2>
          <div class="archive__item-excerpt">
            {{ repository.description | default: "No description available." }}
          </div>
          <p>
            <small>
              {% if repository.language %}
                <strong>Language:</strong> {{ repository.language }} &bull;
              {% endif %}
              <strong>Stars:</strong> {{ repository.stargazers_count }} &bull;
              <strong>Forks:</strong> {{ repository.forks_count }}
            </small>
          </p>
        </article>
      </div>
    {% endif %}
  {% endfor %}
</div>
