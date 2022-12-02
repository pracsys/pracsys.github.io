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
            photo_url: /img/members/ewerton.jpg
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
