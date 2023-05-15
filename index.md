---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

![PejLab group picture](/assets/images/Pejlab_group_pic2.jpg){: .banner}

<br>

We are moving to the [Seattle Children’s Research Institute](https://www.seattlechildrens.org/research/research-institute/) as of May 1st, 2023 where we will be a part of the [University of Washington School of Medicine](https://www.uwmedicine.org/school-of-medicine), and the department of [Genome Sciences](https://www.gs.washington.edu/). We are hiring at all levels.

We are interested in the design of probabilistic machine learning methods and statistical models that incorporate known biochemical principles to facilitate decision-making from limited data and to allow for asking smarter questions. We have a major focus on quantitative analysis of regulatory variation in the human genome from large scale functional genomics data and its application to rare diseases and precision medicine.

<br><br>

{% for person in site.data.members %}
  <div class="person">
    {% if person.image %}
      <img class="person-image" alt="{{ person.name }}" src="/assets/images/people/{{ person.image }}">
    {% endif %}
    <div class="person-info">
      <h2 class="person-name">{{ person.name }}</h2>
      <h4 class="person-title">{{ person.title }}</h4>
      <p>{{ person.bio }}</p>
    </div>
  </div>
{% endfor %}

<br>

# Alumni

{% for person in site.data.alumni %}
  <div class="person">
    {% if person.image %}
      <img class="person-image" alt="{{ person.name }}" src="/assets/images/people/{{ person.image }}">
    {% endif %}
    <div class="person-info">
      <h2 class="person-name">{{ person.name }}</h2>
      <h4 class="person-title">{{ person.title }}</h4>
      <p>{{ person.bio }}</p>
    </div>
  </div>
{% endfor %}
