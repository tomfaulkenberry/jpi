---
layout: default
title: Home
---
{% assign featured_issue = site.issues | where: "featured", true | first %}

<section class="home-hero">
  <div>
    <p class="eyebrow">Current and archival undergraduate scholarship</p>
    <h1>Journal of Psychological Inquiry</h1>
    <p class="lead">A clean, code-first journal website built for straightforward maintenance on GitHub Pages.</p>
    <div class="button-row">
      <a class="button" href="{{ '/submissions/' | relative_url }}">Submit a manuscript</a>
      <a class="button button-secondary" href="{{ '/archives/' | relative_url }}">Browse archives</a>
    </div>
  </div>
  <aside class="hero-panel card">
    <p class="eyebrow">At a glance</p>
    <ul class="checklist">
      <li>Static GitHub Pages deployment</li>
      <li>One shared layout system</li>
      <li>Issue archive generated from collection files</li>
      <li>Minimal CSS, easy to edit by hand</li>
    </ul>
  </aside>
</section>

<section class="feature-grid">
  <article class="card">
    <p class="eyebrow">About the journal</p>
    <h2>Focused, readable, and professional</h2>
    <p>This starter emphasizes a restrained editorial look: clear typography, stable navigation, and an issue-first archive structure that will age well over time.</p>
  </article>
  <article class="card">
    <p class="eyebrow">For authors</p>
    <h2>Submission information is easy to find</h2>
    <p>Core submission details, article types, process expectations, and policy links live in predictable places rather than being buried in uploaded PDFs.</p>
  </article>
  <article class="card">
    <p class="eyebrow">For editors</p>
    <h2>Update the site with simple files</h2>
    <p>Add a new issue by uploading the PDF and creating a single Markdown record in <code>_issues/</code>. The archive page updates automatically.</p>
  </article>
</section>

{% if featured_issue %}
<section class="current-issue card">
  <div>
    <p class="eyebrow">Featured issue</p>
    <h2>{{ featured_issue.title }}</h2>
    <p class="lead">Volume {{ featured_issue.volume }}, Number {{ featured_issue.number }} · {{ featured_issue.season }} {{ featured_issue.year }}</p>
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
    <p class="eyebrow">Editorial workflow</p>
    <h2>Recommended maintenance pattern</h2>
    <ol>
      <li>Update static pages such as editorial board and submissions in Markdown.</li>
      <li>Add new issue metadata in <code>_issues/</code>.</li>
      <li>Upload issue PDFs into <code>assets/pdf/</code>.</li>
      <li>Push changes to GitHub for GitHub Pages to publish.</li>
    </ol>
  </article>
  <article class="card">
    <p class="eyebrow">Suggested next steps</p>
    <h2>What to customize first</h2>
    <ul>
      <li>Replace placeholder copy with the journal’s official scope and submission language.</li>
      <li>Add the complete archive of past issues.</li>
      <li>Insert the real editorial board and office contact details.</li>
      <li>Point the site to a custom domain if desired.</li>
    </ul>
  </article>
</section>
