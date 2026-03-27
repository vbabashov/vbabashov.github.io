---
layout: home
permalink: /
title: "Vusal Babashov"
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

<!-- Hero Section -->
<section class="hero">
  <h1 class="hero__title">I build applied AI, forecasting, and decision systems for complex real-world problems.</h1>
  <p class="hero__subtitle">Applied Scientist with expertise across machine learning, optimization, simulation, and time-series forecasting — turning analytical methods into operational solutions.</p>
  <div class="hero__cta-group">
    <a href="{{ base_path }}/work/" class="hero__cta hero__cta--primary">View Work</a>
    <a href="{{ base_path }}/resume/" class="hero__cta hero__cta--secondary">Resume</a>
    <a href="https://github.com/vbabashov" class="hero__cta hero__cta--secondary" target="_blank"><i class="fab fa-github" aria-hidden="true"></i> GitHub</a>
    <a href="https://linkedin.com/in/vusalbabashov" class="hero__cta hero__cta--secondary" target="_blank"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>
  </div>
</section>

<hr class="section-divider">

<!-- Capabilities Section -->
<section class="home-section">
  <h2 class="home-section__title">What I Do</h2>
  <p class="home-section__subtitle">Core capability areas across applied AI/ML and decision science.</p>

  <div class="capabilities">
    <div class="capability-card">
      <span class="capability-card__icon">🤖</span>
      <h3 class="capability-card__title">Applied AI &amp; LLM Solutions</h3>
      <p class="capability-card__desc">Building AI-powered applications including LLM-enabled product question-answering systems and intelligent automation.</p>
    </div>
    <div class="capability-card">
      <span class="capability-card__icon">📊</span>
      <h3 class="capability-card__title">Machine Learning &amp; Predictive Analytics</h3>
      <p class="capability-card__desc">Regression, classification, and ensemble methods for prediction tasks across finance, healthcare, and operations.</p>
    </div>
    <div class="capability-card">
      <span class="capability-card__icon">📈</span>
      <h3 class="capability-card__title">Forecasting &amp; Time-Series</h3>
      <p class="capability-card__desc">Classical and deep learning approaches for demand forecasting, including STL, TBATS, LSTM, and gradient boosting.</p>
    </div>
    <div class="capability-card">
      <span class="capability-card__icon">⚙️</span>
      <h3 class="capability-card__title">Optimization &amp; Decision Systems</h3>
      <p class="capability-card__desc">Mathematical optimization, simulation, dynamic programming, and multi-criteria decision analysis for operational decision-making.</p>
    </div>
  </div>
</section>

<hr class="section-divider">

<!-- Featured Work Section -->
<section class="home-section">
  <h2 class="home-section__title">Featured Work</h2>
  <p class="home-section__subtitle">Selected projects demonstrating applied problem-solving across domains.</p>

  <div class="work-grid">
    {% assign featured_work = site.work | where: "featured", true | sort: "sort_order" %}
    {% for post in featured_work %}
      <a href="{{ base_path }}{{ post.url }}" class="work-card">
        {% if post.category %}
          <div class="work-card__category">{{ post.category }}</div>
        {% endif %}
        <h3 class="work-card__title">{{ post.title }}</h3>
        <p class="work-card__excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% if post.methods %}
          <div class="work-card__tags">
            {% for method in post.methods limit:4 %}
              <span class="work-card__tag">{{ method }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </a>
    {% endfor %}
  </div>
</section>

<hr class="section-divider">

<!-- Selected Research Section -->
<section class="home-section">
  <h2 class="home-section__title">Selected Research</h2>
  <p class="home-section__subtitle">Peer-reviewed publications in healthcare analytics, optimization, and AI.</p>

  <ul class="research-list">
    {% for post in site.publications reversed limit:3 %}
      <li class="research-list__item">
        <div class="research-list__title">
          <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
        </div>
        {% if post.venue %}
          <div class="research-list__meta">{{ post.venue }}{% if post.date %}, {{ post.date | date: "%Y" }}{% endif %}</div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>

  <p style="margin-top: 1rem;"><a href="{{ base_path }}/research/">View all research →</a></p>
</section>

<hr class="section-divider">

<!-- About Brief Section -->
<section class="home-section">
  <h2 class="home-section__title">About</h2>
  <div class="about-brief">
    <p>I'm an Applied Scientist with a PhD in Operations Research and a background in engineering and statistics. I specialize in using machine learning, optimization, simulation, and forecasting to solve complex business and operational problems across healthcare, finance, and technology.</p>
    <p>My work bridges research rigor with practical implementation — from dynamic programming models for patient scheduling to deep learning pipelines for demand forecasting. I'm driven by the challenge of turning analytical methods into systems that support better real-world decisions.</p>
  </div>
</section>

<hr class="section-divider">

<!-- Footer CTA Section -->
<section class="footer-cta">
  <h2 class="footer-cta__title">Let's Connect</h2>
  <p class="footer-cta__text">Interested in collaboration, speaking, or discussing applied AI/ML work?</p>
  <div class="footer-cta__links">
    <a href="mailto:vbabashov@gmail.com"><i class="fas fa-envelope" aria-hidden="true"></i> Email</a>
    <a href="https://github.com/vbabashov" target="_blank"><i class="fab fa-github" aria-hidden="true"></i> GitHub</a>
    <a href="https://linkedin.com/in/vusalbabashov" target="_blank"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>
    <a href="https://scholar.google.ca/citations?user=GQ9CSjgAAAAJ&hl=en" target="_blank"><i class="fas fa-graduation-cap" aria-hidden="true"></i> Google Scholar</a>
  </div>
</section>


