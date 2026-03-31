---
layout: default
title: Home
---
{% assign featured_issue = site.issues | where: "featured", true | first %}

<section class="home-hero">
  <div>
    <p class="eyebrow">Peer-reviewed undergraduate research in psychology</p>
    <h1>Journal of Psychological Inquiry</h1>
    <p class="lead"><em>Journal of Psychological Inquiry</em> (JPI) is a <b>peer-reviewed</b> journal dedicated to showcasing undergraduate work in psychology and supporting emerging scholars across a wide range of psychological topics, methods, and perspectives.</p>
    <div class="button-row">
      <a class="button" href="{{ '/submissions/' | relative_url }}">Submit a manuscript</a>
      <a class="button button-secondary" href="{{ '/archives/' | relative_url }}">Browse archives</a>
    </div>
  </div>
  <aside class="hero-panel card">
    <p class="eyebrow">Benefits of publishing in JPI</p>
    <ul class="checklist">
      <li>Peer-reviewed journal for undergraduate scholarship</li>
      <li>Accepts rolling submissions</li>
      <li>Multiple article types welcomed</li>
      <li>Current and archived issues available online</li>
    </ul>
  </aside>
</section>

<section class="feature-grid">
  <article class="card">
    <p class="eyebrow">About the journal</p>
    <h2>Undergraduate research in psychology</h2>
    <p>JPI provides a professional, supportive venue for undergraduate research in psychology, including empirical studies, literature reviews, historical work, and other forms of student-centered inquiry.</p>
  </article>
  <article class="card">
    <p class="eyebrow">For authors</p>
    <h2>Submission instructions</h2>
    <p>Authors can find submission requirements, article types, review expectations, and policy information in one place, with links to current guidelines and the journal’s submission process.</p>
    <p><a class="button button-secondary" href="{{ '/submissions/' | relative_url }}">Submissions</a></p>

  </article>
  <article class="card">
    <p class="eyebrow">Archives</p>
    <h2>Browse past and current issues</h2>
    <p>The archive provides issue pages, tables of contents, and downloadable PDFs so readers can easily explore the journal’s history and recent publications.</p>
    <p><a class="button button-secondary" href="{{ '/archives/' | relative_url }}">Archives</a></p>

  </article>
</section>

{% if featured_issue %}
<section class="current-issue card">
  <div>
    <p class="eyebrow">Latest issue</p>
    <h2>{{ featured_issue.title }}</h2>
    <p class="lead">Volume {{ featured_issue.volume }}, Number {{ featured_issue.number }} ({{ featured_issue.year }})</p>
    <p>{{ featured_issue.summary }}</p>
    <div class="button-row">
      <a class="button" href="{{ featured_issue.url | relative_url }}">View issue page</a>
      <a class="button button-secondary" href="{{ featured_issue.pdf | relative_url }}">Download PDF</a>
    </div>
  </div>
</section>
{% endif %}

<section class="home-columns">
  <article class="card">
    <p class="eyebrow">Editorial information</p>
    <h2>Board, policies, and submission standards</h2>
    <p>Learn more about the journal’s editorial board, submission expectations, authorship requirements, and publication policies.</p>
    <p><a class="button button-secondary" href="{{ '/editorial-board/' | relative_url }}">Editorial Board</a></p>
  </article>
  <article class="card">
    <p class="eyebrow">Contact</p>
    <h2>Questions about the journal?</h2>
    <p>For questions about submissions, editorial matters, or the journal’s operations, visit the contact page for current information.</p>
    <p><a class="button button-secondary" href="{{ '/contact/' | relative_url }}">Contact</a></p>
  </article>
</section>

