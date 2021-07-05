---
title: Jobs
layout: none
---


<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  {% assign mycss = "/assets/css/main.css" %}
  <link rel="stylesheet" href= "{{ mycss | relative_url }}">
</head>

<div id = "Homepage">
  {% include header.html %}
  <section class="sec1">
    <div class = "logo_container">
      {% assign myLogo = "/assets/images/Frame1.png" %}
      <img class = "comp_logo" src="{{ myLogo | relative_url }}">
      <span id = "innovate">Innovation happens when you are free to experiment.</span>
      <span id = "leap">The leap toward innovation can seem giant, but with daily practice it will eventually happen.</span>
    </div>
    {% assign myImg = "/assets/images/Rectangle1.png" %}
    <img class = "landing_img" src="{{ myImg | relative_url }}">
  </section>

  <section class="sec2">
    <div id="job_list">
      <h1 id = "job_lst_txt" >Available jobs</h1>
      <div  class="uk-margin uk-card uk-card-default uk-card-body">
        {% for job in site.jobs %}
          <h2>
            <a href="{{ job.url | relative_url }}" >
              {{ job.title }}
            </a>
          </h2>
          <p>{{ job.description | markdownify }}</p>
          <div id="job_info_row">
            <p><b>Keywords: </b>{{ job.Keywords  }}</p>
            <p><b>Location: </b>{{ job.location  }}</p>
            <p><b>Seniority:</b> {{  job.Seniority  }}</p>
          </div>
          <div id="job_lst_line"> </div>
       {% endfor %}
      </div>
    </div>
  </section>
  
  <section class="sec3">
    <div id="subscribe">
      <span id="sub_text">Subscribe to get alerts</span>
      <p>No job listed above for you? You can create a job alert and we will send you an e-mail when a position you are interested becomes available.</p>
      <button id="get_notified" id= "btnApply" onclick="window.location.href='https://forms.office.com/r/QSCWNvEukh'">Get notified</button>
    </div>
  </section>
  {% include footer.html %}
</div>

