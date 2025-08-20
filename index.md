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
             src="{{site.baseurl}}img/people/8602.jpg" style="float:right;height:200px;"/>

<h1>Hsin-Mu (Michael) Tsai - 蔡欣穆</h1>
<br/>

<p>Deputy Vice President for <a href="http://www.aca.ntu.edu.tw" target="_blank">Academic Affairs</a> - 副教務長</p> 

<p>Director, <a href="https://www.dlc.ntu.edu.tw/" target="_blank">Center for Teaching and Learning Development, Digital Learning Center</a>, and <a href="https://aaoffice.ntu.edu.tw/" target="_blank">Academic Advising Office</a> - 教學發展中心/數位學習中心/學習規劃辦公室 主任</p>

<p>Director, <a href="https://iox.ntu.edu.tw/" target="_blank">NTU IoX Center</a> - 臺大智慧聯網研究中心 主任</p> 

<p>Academic Advancement Young Chair Professor - 學術勵進青年講座,<br/> <a href="http://www.csie.ntu.edu.tw/" target="_blank"> Computer Science and Information Engineering</a> </p>
    
<a href="http://www.ntu.edu.tw/" target="_blank">National Taiwan University</a>

<br/> 
<br/> 
</div>

Note: Some information can still be found on my <a href="http://www.csie.ntu.edu.tw/~hsinmu/wiki/">old web site</a>.

__有興趣加入我的研究團隊的碩士班新生，請閱讀<a href="https://hackmd.io/@usfbmh5OQjawM_SraJJSaQ/Hkaf4HkB6" target="_blank">這個</a>。__

<h2> What I do </h2>

* __Research__: I enjoy designing and buidling prototypes and doing hands-on work by myself and with my students. Topics I am interested in include communications and positioning using light, sensing with mobile systems and within cars, and wireless communications and networking in general. See my research page. 
* __Industry Collaboration__: I am currently the Director of <a href="http://iox.ntu.edu.tw/" target="_blank">__NTU IoX Center__</a>. In addition, I have an ongoing research collaboration with EVA Air on applying AI on flight safety data analysis.
* __Digital Learning__: I spent a portion of my time leading a <a href="http://www.dlc.ntu.edu.tw/tech/">team</a> at NTU's <a href="http://dlc.ntu.edu.tw/">Digital Learning Center</a> to develop the university's next-generation learning platform - <a href="https://www.dlc.ntu.edu.tw/ntu-cool/">NTU COOL</a>. See a <a href="https://youtu.be/tW_Edaqv5BM">video</a> about us. I am also leading the <a href="https://www.aca.ntu.edu.tw/w/aca/CIMD">Computer Information Management Division</a> to transform some of the older information systems at the Office of Academic Affairs.
* __NASA__: In 2012, I founded a team with mainly undergraduate students, called NASA (Network Administration and System Administration), to maintain the IT infrastructure in our department. Currently I am still teaching a course to train these students.
 


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






<h2> Select Honors </h2>
* 2023 National Taiwan Univeristy Academic Advancement Young Chair Professorship (台大學術勵進青年講座教授) <br/> (Awarded to only 15 out of 2000+ full-time faculty members in NTU)
* 2023 Young Scholar Innovation Award, Foundation for the Advancement of Outstanding Scholarship, Taiwan
 (年輕學者創新獎, 傑出人才發展基金會)
* 2020 National Taiwan University Distinguished University Service Award (台大校內傑出服務獎) <br/> (for my contribution in leading the NTU COOL team to cope with the growing online teaching demand during the COVID-19 pandemic)
* 2019-2021 Outstanding Young Scholar Grant, Ministry of Science and Technology, Taiwan (科技部優秀年輕學者計畫)
* 2018 Delta Research Excellence Award (台達傑出研究獎)
* 2018 Jen-Min Distinguished Young Scholar Chair Professorship (仁民傑出青年學者講座)
* 2017 NTU EECS Academic Achievement Award (電機資訊學院學術貢獻獎)
* 2015 ACM Taipei Chapter K. T. Li Young Researcher Award (李國鼎青年研究獎)
* 2014 Intel Labs Distinguished Collaborative Research Award 
* 2013 Intel Labs Early Career Faculty Honor Program Awardee <br/>
(__first__ to receive the honor outside of Europe and North America) 
* 2013 National Taiwan University Distinguished Teaching Award (台大教學傑出獎)<br/>
(awarded to __1%__ of the university faculty)


<h2> Research Interests </h2> 
* Visible light communications and positioning
* Vehicular networking and communications
* Vehicle and transportation systems


<section>
    <h2>Research Projects [updating] </h2>
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
