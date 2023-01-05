---
layout: page
title: Robots
subtitle:
members:       
  - name: Owned by PRACSYS Lab
    list:
      - full: true
        list:
          - name: Baxter
            photo_url: /img/robots/Baxter.jpg
            web_url: https://robots.ieee.org/robots/baxter/ 
          - name: Yaskawa Motoman
            photo_url: /img/robots/Motoman.png
            web_url: https://www.motoman.com/en-us
          - name: Omnidirectional
            photo_url: /img/robots/Omnidirectional.png
            web_url: https://robots.ieee.org/robots/baxter/ 
          - name: Tensegrity
            photo_url: /img/robots/tensegrity.jpeg
            web_url: https://www.nasa.gov/content/super-ball-bot/
          - name: 2-Finger Adaptive Robotiq Gripper
            photo_url: /img/robots/robotiq.jpeg
            web_url: https://robotiq.com/products/2f85-140-adaptive-robot-gripper
          - name: 3-Finger Adaptive Robotiq Gripper
            photo_url: /img/robots/robotiq2.jpeg
            web_url: https://robotiq.com/products/3-finger-adaptive-robot-gripper
          


  - name: Owned by collaborators
    list:
      - full: true
        list:
          - name: KUKA Iiwa LBR (owned by Dr. Abdeslam Boularias's Lab)
            photo_url: /img/robots/Kuka_Photo.jpg
            web_url: https://www.kuka.com/en-de/products/robot-systems/industrial-robots/lbr-iiwa
          - name: Motiv's Robomantis (owned by Dr. Abdeslam Boularias's Lab)
            photo_url: /img/robots/Robomantis.png
            web_url: https://motivss.com/tech-dev/robomantis/
          - name: UR5 (owned by Dr.Jingjin Yu's Lab)
            photo_url: /img/robots/UR5.png
            web_url: https://www.universal-robots.com/products/ur5-robot/
          - name: Underactuated Adaptive OpenHand (owned by Dr. Aaron Dollar's Lab)
            photo_url: /img/robots/ModelQ.png
            web_url: https://www.eng.yale.edu/grablab/openhand/

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
