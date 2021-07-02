---
title: Jobs

---
<head>
{% assign mycss = "{{ site.baseurl }}/assets/css/main.css" %}
<link rel="stylesheet" href= "{{ mycss | relative_url }}">
</head>
<header>
{% include header.html %}
</header>
<div>
{% assign myLogo = "{{ site.baseurl }}/assets/images/Frame1.png" %}
<img class = "comp_logo" src="{{ myLogo | relative_url }}">
</div>
<br><br>
<div>
{% assign myImg = "{{ site.baseurl }}/assets/images/Rectangle1.png" %}
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

