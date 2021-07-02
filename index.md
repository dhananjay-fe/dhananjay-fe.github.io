---
title: Jobs

---
<head>
{% assign mycss = "/assets/css/main.css" %}
<link rel="stylesheet" href= "{{ mycss | relative_url }}">
</head>
{% include header.html %}
<div>
{% assign myLogo = "/assets/images/Frame1.png" %}
<img class = "comp_logo" src="{{ myLogo | relative_url }}">
</div>
<br><br>
<div>
{% assign myImg = "/assets/images/Rectangle1.png" %}
<img class = "landing_img" src="{{ myImg | relative_url }}">
</div>
<h1>Jobs listing:</h1>
<div  class="uk-margin uk-card uk-card-default uk-card-body">
{% for job in site.jobs %}
  <h2>
    <a href="{{ job.url | relative_url }}">
      {{ job.title }}
    </a>
  </h2>
  <p>{{ job.description | markdownify }}</p>
  <p>Published on: {{ job.published  }}</p>
{% endfor %}
</div>
{% include footer.html %}

