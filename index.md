---
layout: page
title: "Home"
class: home
---
<body style=""><path>



<div class="columns" markdown="1">

# Hi, I'm Yanna Lin

</div>

<div class="columns" markdown="1">

<div class="intro" markdown="1">

I am a Postdoctoral Researcher at the University of Waterloo, working with [Prof. Jian Zhao](https://www.jeffjianzhao.com) in the [WVisdom research lab](https://www.jeffjianzhao.com/team).

Before joining Waterloo, I worked as a Postdoctoral Researcher and obtained my Ph.D. in Computer Science and Engineering from the Hong Kong University of Science and Technology (HKUST), under the supervision of [Prof. Huamin Qu](http://www.huamin.org) in the [VisLab](http://vis.cse.ust.hk). 
My Ph.D. was supported by the [Hong Kong PhD Fellowship Scheme](https://cerg1.ugc.edu.hk/hkpfs/index.html) and recognized with the [HKUST RedBird Academic Excellence Award](https://fytgs.hkust.edu.hk/admissions/Admission-to-Hong-Kong-Campus/submitting-an-application/scholarships-and-fees) for three consecutive years.
I earned my Bachelor’s Degree in Software Engineering from Sun Yat-sen University, ranked 1/447.
During my undergraduate studies, I was honored with the National Scholarship for three consecutive years (top 0.5%).

My research interests include data visualisation and human-AI collaboration. I focus on designing intuitive interfaces and developing algorithms to enhance data communication and analysis, and facilitate data-driven decision-making.


<span style="background-color:#f4ecfc; font-weight: bold;">I am on the job market. Please contact me if you have any relevant positions or opportunities:) </span>

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/lala4.1.JPG' type='image/webp' />
  <img
    src='/images/lala4.1.JPG'
    alt='Yanna Lin'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
<!-- * NSH 2602B -->
</div>

</div>

<!-- ## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a> -->

<!-- ## Featured Publications -->

<div class="columns" markdown="1">
## Publications 
</div>
{% assign highlighted = site.publications | where_exp: "p", "p.highlight == true" %}
{% assign pubyears = highlighted | group_by:"year" %}
{% assign sorted_pubyears = pubyears | reverse %}
{% for year in sorted_pubyears %}
 <h2 class="publicationyear" href="#y{{ year.name }}"><span> {{ year.name }} </span> </h2>
{% for pub in year.items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

<script>
  {% include itemsjs.min.js %}
  {% include pubfilter.js %}
</script>


<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul class="scroll-bar">
{% for news in site.data.news limit:10 %}
  {% include news.html news=nelows %}
{% endfor %}
</ul>

</div>

<div class="award" markdown="1">
## Awards

  <ul class="scroll-bar">
    {% assign future_award = site.data.awards | where_exp:'item','item.start == null' %}
    {% for award in future_award %}
      {% include award.html award=award %}
    {% endfor %}
  </ul>

</div>

</div>


    <!-- JS Begins -->
    <script src="lib/jquery.min.js"></script>
    <script src="lib/paper.js"></script>
    <script src="jelly.js"></script>
    <script src="tentacle.js"></script>
    <script src="main.js"></script>
    <!-- JS Ends -->
  </path>

</body>
