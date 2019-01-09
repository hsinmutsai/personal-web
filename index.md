---
layout: default
title: Home
notitle: true

# groups of columns of {roles: list, width: num, image: bool}
role-tables:
- - roles: [faculty, postdoc, staff]
    width: 4
    image: true
  - roles: [grad]
    width: 8
    image: true
- - roles: [collab, ugrad, ugrad-alum]
    width: 5
    image: false
  - roles: [alum]
    width: 7
    image: false

---



<div class="jumbotron"> 
    <!--<img src="img/people/proftsai.png" height=250 align="right"/>-->
   <img class="rounded-circle profile"          
             src="{{site.baseurl}}img/people/proftsai2.jpg" style="float:right;height:200px;"/>

    <h1>Hsin-Mu (Michael) Tsai - 蔡欣穆</h1>

    Associate Professor, <br/> Computer Science and Information Engineering <br/>
    National Taiwan University


<br/>    
<br/> 
<br/> 
</div>

<h2> Research Interests </h2> 
* Visible light communications and positioning
* Vehicular networking and communications
* Vehicle and transportation systems



<h2> Select Honors </h2>
* 2018 Delta Research Excellence Award
* 2018 Jen-Min Young Scholar Chair Professorship
* 2017 NTU EECS Academic Achievement Award
* 2015 ACM Taipei Chapter K. T. Li Young Researcher Award
* 2014 Intel Labs Distinguished Collaborative Research Award
* 2013 Intel Labs Early Career Faculty Honor Program Awardee <br/>
(__first__ to receive the honor outside of Europe and North America) 
* 2013 National Taiwan University Distinguished Teaching Award <br/>
(awarded to __1%__ of the university faculty)


<section>
    <h2>Research</h2>
    <div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.status != "inactive" %}
                {% include project-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>
</section>


<section>
    <h2>News</h2>
    <ul class="news list-unstyled">
        {% for post in site.posts limit: site.front_page_news %}
            {% include news-item.html item=post %}
        {% endfor %}
    </ul>
    {% assign numposts = site.posts | size %}
    {% if numposts >= 1 %}
        <p>
            <span class="fa fa-fw fa-history"></span>
            <a href="{{ site.baseurl }}blog.html">Older posts&hellip;</a>
        </p>
    {% endif %}
</section>

<h3>Misc. Information</h3>
* [My Google Scholar Profile](https://scholar.google.com/citations?user=RL0CmuAAAAAJ&hl=en)
* Office: CSIE Building R316
* Phone: +886 2 33664888 ext. 316

<!--
<div id="people">
    <h2>People</h2>
    {% for role-table in page.role-tables %}
        <section class="people row justify-content-between">
            {% for role-column in role-table %}
                <div class="col-md-{{ role-column.width }}">
                    {% for role in role-column.roles %}
                        {% include role-people.html role=role image=role-column.image %}
                    {% endfor %}
                </div>
            {% endfor %}
        </section>
    {% endfor %}
</div>
-->