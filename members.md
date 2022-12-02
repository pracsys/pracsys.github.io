---
layout: page
title: Members
subtitle:
members:
  - name: Faculty
    list:
      - full: true
        list:
          - name: Kostas Bekris
            photo_url: /img/members/bekris.png
            web_url: https://robotics.cs.rutgers.edu/pracsys/members/kostas-bekris/
  - name: Current members
    list:
      - name: Post-Docs
        full: true
        list:
          - name: Ewerton Vieira
            photo_url: /img/members/ewerton.jpg
            web_url: https://ewerton-vieira.github.io/
          - name: Troy McMahon
            photo_url: /img/members/troy.jpg
            web_url: https://ewerton-vieira.github.io/
      - name: PhD students
        full: true
        list:
          - name: Aravind Sivaramakrishnan 
            photo_url: /img/members/aravind.jpeg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Daniel Nakhimovich 
            photo_url: /img/members/danieln.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Edgar Granados
            photo_url: /img/members/edgarg.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Shiyang Liu
            photo_url: /img/members/shiyangl.jpg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Yinglong Miao
            photo_url: /img/members/yinglongm.jpg
            web_url: https://ylmiao541.github.io/index.html
          - name: Isidoros Marougkas
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Nelson Chen
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Rachel Lai
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Noah Carver
            photo_url: /img/members/noahc.jpg
            web_url: https://noahrcarver.github.io/
  - name: <a name="alumni"></a>Alumni
    list:
      - name: PhD alumni
        full: False
        list:
          - name: Rui Wang -> 
          - name: Kun Wang -> 
          - name: Bowen Wen (Fall 2018 - Spring 2022) -> Nvidia Research, Seattle, WA.
                PhD Thesis: “Beyond Instance-level Reasoning in Object Pose Estimation and Tracking for Robotic Manipulation”
          - name: Chaitanya Mitash  (Fall 2015 - Summer 2020) (co-advised with Abdeslam Boularias) -> Amazon Robotics, Boston, MA.
		PhD Thesis: “Scalable, Physics-aware 6D Pose Estimation for Robot Manipulation”
          - name: Rahul Shome (Fall 2013 - Spring 2020) ->  PostDoc at Rice University -> Faculty, Australian National University (ANU)
		PhD thesis: “The Problem of Many: Efficient Multi-arm, Multi-object Task and Motion Planning with Optimality Guarantees”	
          - name: Andrew Kimmel (Fall 2012 - Summer 2019) -> Amazon Robotics, Boston, MA.
		All But Dissertation 
          - name: Zachary Littlefield (Fall 2012 - Fall 2019), NASA STR Fellow -> Uber Robotics, Pittsburgh, PA -> Aurora 
		PhD Thesis: “Efficient and Asymptotically Optimal Kinodynamic Motion Planning”
          - name: Thanasis Krontiris (Fall 2012 - Summer 2017) -> Autonomous driving start-up “Auto X” , Palo Alto, CA -> Google
		PhD Thesis: “Hierarchical Frameworks for Efficient Prehensile Rearrangement with a Robotic Manipulator”
          - name: Andrew Dobson (Fall 2012 - Summer 2017), A DHS fellow -> PostDoc at University of Michigan, Ann Arbor -> State of CA.
		PhD Thesis: “Compact Representations for Efficient Robot Motion Planning with Formal Guarantees”

   
---

<div class="row">
  {% for big_group in page.members %}
    <h1> {{big_group.name}} </h1>
    {% for group in big_group.list %}
    {% if group.list.size > 0 %}
      {% if group.name %}
        <h2>{{ group.name }}</h2>
      {% endif %}
      {% if group.full %}
      <div class="row member-row">
        {% for member in group.list %}
          <div class="col-xl-3 col-lg-3 col-md-3 text-center col-sm-6 col-xs-6 member-col">
            <a target="_blank" href="{{ member.web_url }}">
              <img class="img-responsive" src="{{ member.photo_url }}" alt="{{member.name}}">
            </a>
            <a target="_blank" href="{{ member.web_url }}">
              {{ member.name }}
            </a>
          </div>
        {% endfor %}
      </div>
      {% else %}
        <ul>
          {% for member in group.list %}
            {% if member.web_url %}
              <li><a href="{{member.web_url}}"> {{member.name}} </a></li>
            {% else %}
              <li><a> {{member.name}} </a></li>
            {% endif %}
          {% endfor %}
        </ul>
      {% endif %}
    <br>
    {% endif %}
    {% endfor %}
  {% endfor %}
</div>


<!-- <h3 id="undergraduate-students">Undergraduate students</h3>
<ul>
</ul>
</div> -->

<!-- <h2 id="collaborators">Collaborators</h2> -->
<!-- <ul>
  <li><a href="https://www.cs.cmu.edu/~astein/">Aaron Steinfeld</a></li>
  <li><a href="https://www.cs.cmu.edu/~kkitani/">Kris Kitani</a></li>
  <li><a href="http://www.lauravherlant.com/">Laura Herlant</a></li>
</ul> -->
