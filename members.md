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
            photo_url: img/members/ewerton.jpg
            web_url: https://ewerton-vieira.github.io/
      - name: PhD students
        full: true
        list:
          - name: Aravind Sivaramakrishnan 
            photo_url: /img/members/aravind.jpeg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Daniel Nakhimovich 
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Edgar Granados
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Shiyang Liu
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Yinglong Miao
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
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
            photo_url: /img/members/ismarou.png
            web_url: https://www.linkedin.com/in/isidoros-marougkas
  - name: <a name="alumni"></a>Alumni
    list:
      - name: PhD alumni
        full: False
        list:
          - name: Rui Wang -> Post-doc with Nick Roy at MIT
            web_url: https://siddancha.github.io/
          - name: Jun Wang -> Post-doc with Pieter Abbeel at UC Berkeley
            web_url: https://xingyu-lin.github.io/
          - name: Bowen Wen (co-advised with Martial Hebert)
            web_url: https://www.ri.cmu.edu/ri-people/brian-e-okorn/

      - name: Master's students (Reseach Master's)
        full: False
        list:
          - name: Chuer Pan (MSR)
            web_url: https://www.ri.cmu.edu/ri-people/chuer-pan/
          - name: Gaurav Pathak (MSR) -> Adobe
            web_url: https://www.ri.cmu.edu/ri-people/gaurav-pathak/
          - name: Zixuan Huang (MSR) -> Michigan PhD
            web_url: https://www.ri.cmu.edu/ri-people/zixuan-huang/
          - name: Yufei Wang (MSCS) -> CMU PhD
            web_url: https://yufeiwang63.github.io/
          - name: Harshit Sikchi (MSCS) -> UT Austin PhD
            web_url: https://hari-sikchi.github.io/
          - name: Sujay Bajrachaya (MSR) -> Software Engineer at Epic Systems
            web_url: https://sujaybajracharya.me/
          - name: Qiao Gu (MSR) -> U Toronto PhD
            web_url: https://georgegu1997.github.io/
          - name: Gautham Narayan Narasimhan (MSME) -> CV / ML Engineer at Path Robotics
            web_url: https://gauthamnarayan.com/
          - name: Jianing (Aurora) Qian (MSR) -> U Penn PhD
            web_url: https://www.ri.cmu.edu/ri-people/jianing-qian/
          - name: Junyu (Jenny) Nan (MSR) -> CMU PhD
            web_url: https://www.ri.cmu.edu/ri-people/junyu-nan/
          - name: Mengyun (Olivia) Xu (MSCS) -> Amazon Robotics
            web_url: https://www.linkedin.com/in/mengyun-olivia-xu-36a7ab126
          - name: Edward Ahn (MSR) -> AI / ML Engineer at Apple
            web_url: https://www.ri.cmu.edu/ri-people/edward-ahn/
    
      - name: Visiting Reseachers
        full: False
        list:
            - name: Himangi Mittal -> CMU MSR
              web_url: https://himangim.github.io/
            - name: Jianren Wang -> CMU PhD
      - name: Master's students (Capstone Project)
        full: False
        list:
          - name: Yi Gu (MRSD)
            web_url: https://www.ri.cmu.edu/ri-people/yi-gu/
          - name: Arpit Jangid (MSCV)
            web_url: https://www.ri.cmu.edu/ri-people/arpit-jangid/
          - name: Ji Liu (MSCV)
            web_url: https://www.ri.cmu.edu/ri-people/ji-liu/
          - name: Zhenli Zhang (MSCV)
            web_url: https://www.linkedin.com/in/zhenli-zhang-a36912126
          - name: Xiaochen Han (MSCV)
            web_url:
          - name: Tanay Sharma (MSCV)
            web_url:

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
