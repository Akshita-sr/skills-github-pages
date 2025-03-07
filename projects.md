---
layout: page
title: Projects
permalink: /projects/
---

# Featured Projects

### [RoboticsML](https://github.com/Akshita-sr/RoboticsML)
- **Description:** A collection of machine learning algorithms for robotics applications.
- **Technologies:** Python, Machine Learning, Robotics
- **Link:** [View on GitHub](https://github.com/Akshita-sr/RoboticsML)

---

# Other Projects

{% for repository in site.github.public_repositories %}
{% if repository.name != "RoboticsML" %}
- [{{ repository.name }}]({{ repository.html_url }}): {{ repository.description | default: "No description available." }}
{% endif %}
{% endfor %}
