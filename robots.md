---
layout: page
title: Members
subtitle:
members:
  - name: Faculty
    list:
      - full: true
        list:
          - name: David Held
            photo_url: /img/members/bekris.png
            web_url: https://davheld.github.io
  - name: Robots
    list:
      - name: Robots
        full: true
        list:
          - name: Baxter
            photo_url: /img/robots/baxter.jpg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Rachel Lai
            photo_url: https://drive.google.com/file/d/1z4ptrKAtr4E-GQle4vtc1Eg0vID_OSZn/view?usp=share_link
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Noah Carver
            photo_url: https://drive.google.com/file/d/1z4ptrKAtr4E-GQle4vtc1Eg0vID_OSZn/view?usp=share_link
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Yufei Wang<br>(co-advised with Zackory Erickson)
            photo_url: https://yufeiwang63.github.io/img/1inch_yufeiwang.jpg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Jenny Wang
            photo_url: https://www.ri.cmu.edu/app/uploads/2021/07/Wang_Jenny-scaled.jpg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
      

     
---

<div class="row">
  {% for big_group in page.robot %}
    <h1> {{big_group.name}} </h1>
    {% for group in big_group.list %}
    {% if group.list.size > 0 %}
      {% if group.name %}
        <h2>{{ group.name }}</h2>
      {% endif %}
      {% if group.full %}
      <div class="row member-row">
        {% for robot in group.list %}
          <div class="col-xl-3 col-lg-3 col-md-3 text-center col-sm-6 col-xs-6 robot-col">
            <a target="_blank" href="{{ robot.web_url }}">
              <img class="img-responsive" src="{{ robot.photo_url }}" alt="{{robot.name}}">
            </a>
            <a target="_blank" href="{{ robot.web_url }}">
              {{ robot.name }}
            </a>
          </div>
        {% endfor %}
      </div>
      {% else %}
        <ul>
          {% for robot in group.list %}
            {% if robot.web_url %}
              <li><a href="{{robot.web_url}}"> {{robot.name}} </a></li>
            {% else %}
              <li><a> {{robot.name}} </a></li>
            {% endif %}
          {% endfor %}
        </ul>
      {% endif %}
    <br>
    {% endif %}
    {% endfor %}
  {% endfor %}
</div>
