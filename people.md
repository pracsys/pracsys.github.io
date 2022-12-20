---
layout: page
title: People
subtitle:
members:
  - name: Current Members
    list:
      - full: true
        list:
          - name: Dr. Kostas Bekris
            photo_url: /img/people/kostasb.jpg
            web_url: https://robotics.cs.rutgers.edu/pracsys/members/kostas-bekris/
          - name: Aravind Sivaramakrishnan
            photo_url: /img/people/aravinds.jpeg
            web_url: https://people.cs.rutgers.edu/as2578/
          - name: Daniel Nakhimovich
            photo_url: /img/people/danieln.jpg
            web_url: 
          - name: Edgar Granados
            photo_url: /img/people/edgarg.png
            web_url: 
          - name: Shiyang Lu
            photo_url: /img/people/shiyangl.jpg
            web_url: 
          - name: Yinglong Miao
            photo_url: /img/people/yinglongm.jpg
            web_url: https://ylmiao541.github.io/index.html
          - name: Isidoros Marougkas
            photo_url: /img/people/isidorosm.jpg
            web_url: https://www.linkedin.com/in/isidoros-marougkas
          - name: Noah Carver
            photo_url: /img/people/noahc.jpg
            web_url: https://noahrcarver.github.io/
          - name: Nelson Chen
            photo_url: /img/people/nelsonc.jpg
            web_url: 
          - name: Rachel Lai
            photo_url: /img/people/rlai.jpg
            web_url: https://rachellai27.github.io/

  - name: <a name="alumni"></a>Alumni
    list:
      - name: PostDoc
        full: False
        list:
          - name: David Surovik
            bio: Postdoctoral Research Associate at University of Oxford.
          - name: Avishai Sintov
            bio: Assistant Professor at Tel-Aviv University.
      - name: Ph.D. Students
        full: False
        list:
          - name: Zakary Littlefield
            bio: 
          - name: Andrew Kimmel
            bio: 
          - name: Rahul Shome
            bio: 
          - name: Chaitanya Mitash
            bio: 
          - name: Kun Wang
            bio: 
          - name: Rui Wang
            bio: 
          - name: Bowen Wen
            bio: 
          - name: Andrew Dobson
            bio: Postdoc at University of Michigan, Ann Arbor.
          - name: Athanasios Krontiris
            bio: Joined Samsung Strategy and Innovation Center.
          - name: Shaojun Zhu
            bio: Joined Argo AI.
      - name: MS Students
        full: False
        list:
          - name: Aniket Anvit
            bio: Joined Bloomberg LP.
          - name: Rajanya Dhar
            bio: Joined Bloomberg LP.
          - name: Ryan Luna
            bio: Joined Lydia Kavraki’s Physical and Biological Computing group at Rice University as a Ph.D. student. – Upon completion of PhD joined Waymo.
          - name: Zacharias Psarakis
            bio: Joined iRobot.
          - name: Colin Rennie
            bio: Joined Jask.
          - name: Min Zhao
            bio: Joined American Express.
          - name: James D. Marble
            bio: Joined Sierra Nevada Corporation.
          - name: Ilias Apostolopoulos
            bio: Joined the research project of Dr. Eelke Folmer and Dr. George Bebis and currently working towards his PhD degree at UNR.
          - name: Yanbo Li
            bio: Joined Noble Studios Inc.
      - name: Undergradautes
        full: False
        list:
          - name: Patrick Meng
            bio: 
          - name: Seth Karten
            bio: 
          - name: Qandeel Sajid
            bio: Continued as a PhD student at USC with Maja Mataric.
          - name: Alexis Oyama
            bio: Joined the MS program of the Entertainment Technology Center at Carnegie Mellon University.
          - name: Ethan Pang
            bio: Joined Micron Technology, Inc.
          - name: Jared Rhizor
            bio: Continuing his studies at the University of Nevada, Reno.
      - name: Staff
        full: False
        list:
          - name: Chris Kourtev
---

<div class="row">
  {% for big_group in page.members %}
    <h1> {{big_group.name}} </h1>
    {% for group in big_group.list %}
    {% if group.list.size > 0 %}
      {% if group.name %}
        <br>
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
        <dl>
          {% for member in group.list %}
            <dt><a> {{member.name}} </a></dt>
            <dd> {{member.bio}} </dd>
          {% endfor %}
        </dl>
      {% endif %}
    <br>
    {% endif %}
    {% endfor %}
  {% endfor %}
</div>
