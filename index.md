---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
permalink: /
---

![PejLab group picture](/assets/images/group_pic.jpg){: .banner}

<div class="hero-panel">
  <p class="hero-kicker">Genomic Data Modeling Lab</p>
  <h1>Statistical machine learning for regulatory genomics, transcriptomics, and rare disease</h1>
  <p>
    The PejLab develops probabilistic and mechanistic models that formalize
    biochemical principles and expert knowledge into quantitative frameworks for
    learning from noisy, limited genomic data.
  </p>
  <p>
    We are based at the <a href="https://www.seattlechildrens.org/research/research-institute/">Seattle Children's Research Institute</a>
    and the <a href="https://www.uwmedicine.org/school-of-medicine">University of Washington School of Medicine</a>,
    with affiliations in <a href="https://www.gs.washington.edu/">Genome Sciences</a>.
    Our work spans regulatory genomics, multimodal transcriptomics, complex trait genetics,
    and transcriptome-forward approaches to rare disease. We are not currently running an open search,
    but we are always interested in exceptional candidates.
  </p>
  <div class="quick-links">
    <a href="/research/">Research</a>
    <a href="/tools-and-data/">Tools and Data</a>
    <a href="/join-us/">Join Us</a>
    <a href="https://scholar.google.com/citations?hl=en&user=PCZVnXYAAAAJ&view_op=list_works&sortby=pubdate">Publications</a>
  </div>
</div>

## Research at a glance

<div class="feature-grid">
  <div class="feature-card">
    <h3>Rare disease genomics</h3>
    <p>We develop transcriptome-forward methods that improve molecular diagnosis when genome or exome sequencing alone is not enough.</p>
  </div>
  <div class="feature-card">
    <h3>Regulatory genomics</h3>
    <p>We build mechanistic models of cis-regulatory variation to quantify how genetic variants alter gene dosage and expression.</p>
  </div>
  <div class="feature-card">
    <h3>Multimodal transcriptomics</h3>
    <p>We design methods that extract richer RNA phenotypes from bulk, long-read, spatial, and single-cell sequencing data.</p>
  </div>
  <div class="feature-card">
    <h3>Complex trait genetics</h3>
    <p>We integrate molecular trait mapping with association studies to connect genetic signals to interpretable biological mechanisms.</p>
  </div>
</div>

## Selected tools and data

<div class="spotlight-grid">
{% for project in site.data.projects limit:4 %}
  <div class="spotlight-card">
    <h3>{{ project.name }}</h3>
    <p>{{ project.description }}</p>
    <p class="spotlight-links">
      {% for link in project.links limit:3 %}
        <a href="{{ link.url }}">{{ link.name }}</a>{% unless forloop.last %} <span>•</span> {% endunless %}
      {% endfor %}
    </p>
  </div>
{% endfor %}
</div>

## Recent highlights

<div class="highlight-list">
  <div class="highlight-item">
    <h3>Recent methods papers</h3>
    <p><a href="https://www.nature.com/articles/s41467-024-54840-8">Pantry</a> and <a href="https://www.nature.com/articles/s41467-024-44710-8">aFC-n / haplotype-aware modeling</a> extended our work on RNA phenotypes and regulatory effect-size estimation.</p>
  </div>
  <div class="highlight-item">
    <h3>Public data resources</h3>
    <p>We maintain public tools and datasets including Pantry, ANEVA, aFC-n, and RatGTEx for broader use by the community.</p>
  </div>
  <div class="highlight-item">
    <h3>Prospective trainees and researchers</h3>
    <p>We are always interested in hearing from exceptional candidates with strong scientific programming backgrounds across genomics, statistical genetics, machine learning, and probabilistic modeling.</p>
  </div>
</div>

<br><br>

## Current lab members

{% for person in site.data.members %}
  <div class="member">
    {% if person.image %}
      <img class="person-image" alt="{{ person.name }}" src="/assets/images/people/{{ person.image }}">
    {% endif %}
    <div class="person-info">
      <h2 class="person-name">{{ person.name }}</h2>
      <h4 class="member-title">{{ person.title }}</h4>
      <p>{{ person.bio }}</p>
    </div>
  </div>
{% endfor %}

<br>

<details class="alumni-toggle">
  <summary>Alumni</summary>
  {% for person in site.data.alumni %}
    <div class="alum">
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <h4 class="alum-title">{{ person.title }}</h4>
        <p>{{ person.bio }}</p>
      </div>
    </div>
  {% endfor %}
</details>
