---
layout: page
title: Reviews
description: Rates and simple review of books and movies.
image: assets/images/pic11.jpg
nav-menu: true
---

<div id="main" class="alt">

    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Reviews / 书影音</h1>
            </header>
            <p>Rates and simple review of books and movies.</p>
        </div>
    </section>

    <section id="two" class="spotlights">
        {% for post in site.categories.reviews %}
        <section>
            <a href="{{ post.url | relative_url }}" class="image">
                {% if post.image %}
                    <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" data-position="center center" />
                {% else %}
                    <img src="{{ 'assets/images/pic11.jpg' | relative_url }}" alt="" data-position="center center" />
                {% endif %}
            </a>
            
            <div class="content">
                <div class="inner">
                    <header class="major">
                        <h3>{{ post.title }}</h3>
                        <div class="rating" style="color: #f39c12; margin-bottom: 1em; font-weight: bold;">
                            Rating：{{ post.rating | default: "N/A" }}
                        </div>
                    </header>
                    
                    <p>{{ post.description | default: "Read full" }}</p>
                    
                    <ul class="actions">
                        <li><a href="{{ post.url | relative_url }}" class="button">Read full</a></li>
                    </ul>
                </div>
            </div>
        </section>
        {% else %}
        <div class="inner">
            <p style="padding: 2em; border: 1px dashed #ffffff; text-align: center;">
                目前还没有发布任何书评或影评。
            </p>
        </div>
        {% endfor %}
    </section>

</div>
