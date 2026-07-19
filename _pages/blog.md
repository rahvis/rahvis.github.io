---
layout: archive
title: "Blog"
permalink: /blog/
description: "Blog by Rahul Vishwakarma (Research Engineer at WorkOnward, IEEE Senior Member, BCS Fellow) on machine learning, generative AI, agentic AI, multi-agent systems, conformal prediction, and enterprise technology."
keywords: "Rahul Vishwakarma blog, agentic AI blog, machine learning blog, generative AI articles, multi-agent systems, conformal prediction, AI engineering, enterprise AI"
author_profile: true
---

{% include base_path %}

Essays and engineering notes on machine learning, generative AI, agentic systems, and building reliable AI for the enterprise.
Subscribe via the <a href="{{ base_path }}/feed.xml" target="_blank" rel="noopener">RSS feed</a>.

<div class="blog-list">
  {% for post in site.posts %}
  <article class="blog-list__row" itemscope itemtype="https://schema.org/BlogPosting" style="padding: 1em 0; border-bottom: 1px solid #f2f3f3;">
    <h2 class="archive__item-title" itemprop="headline" style="margin-top: 0; margin-bottom: 0.25em;">
      <a href="{{ post.url | prepend: base_path }}" target="_blank" rel="noopener" itemprop="url">{{ post.title }}</a>
    </h2>
    <p class="page__meta" style="margin: 0 0 0.5em;">
      <i class="fa fa-calendar" aria-hidden="true"></i>
      <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%B %-d, %Y" }}</time>
      {% if post.read_time %} &nbsp;&middot;&nbsp; {% include read-time.html %}{% endif %}
    </p>
    {% if post.description %}
    <p class="archive__item-excerpt" itemprop="description" style="margin: 0;">{{ post.description }}</p>
    {% elsif post.excerpt %}
    <p class="archive__item-excerpt" itemprop="description" style="margin: 0;">{{ post.excerpt | markdownify | strip_html | truncate: 200 }}</p>
    {% endif %}
  </article>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
<p>New posts are coming soon.</p>
{% endif %}
