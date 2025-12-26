---
layout: page
title: "Home"
class: home
---
<body style=""><path>



<div class="columns" markdown="1">

# Hi, I'm Zhaocong Yang

</div>

<div class="columns" markdown="1">

<div class="intro" markdown="1">

I am a final-year PhD Candidate in Department of Computer Science at the University of North Carolina at Charlotte, under the supervision of [Prof. Jing Yang](https://cci.charlotte.edu/directory/jing-yang/). My research interests include the intersection of visual analytics, human–agent collaboration, and Artificial Intelligence, with a particular focus on designing interactive systems that help people reason about complex data and models. My research explores how visualization and intelligent agents (e.g., recommendation systems and large language models) can work together to support sensemaking, decision-making, and exploratory analysis.

Before starting my PhD, I earned my Bachelor’s and Master's Degrees in Computer Science and Mathematics & Statistics from the University of North Carolina at Charlotte, where I was dual-enrolled with Early-Enrty Master in Computer Science program. 

In parallel with my academic research, I have worked as a research intern at Toyota Racing Development USA, where I developed visual analytics tools to support aerodynamic analysis and engineering decision-making. I am passionate about building systems that bridge theory and practice, enabling domain experts to better understand data and models in real-world settings. 


<span style="background-color:#f4ecfc; font-weight: bold;">I am on the job market. Please contact me if you have any relevant positions or opportunities:) </span>

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/zhaocong.png' type='image/webp' />
  <img
    src='/images/zhaocong.png'
    alt='Zhaocong Yang'>
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
