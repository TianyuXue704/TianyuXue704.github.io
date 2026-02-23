---
layout: page
title: Reviews
description: about books and movies
image: assets/images/pic11.jpg
nav-menu: true
---

<div id="main" class="alt">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>contents</h1>
            </header>
            <p>Rates and simple review of books and movies.</p>
        </div>
    </section>

    <section id="two" class="spotlights">
        {% for post in site.categories.reviews %}
        <section>
            <a href="{{ post.url | relative_url }}" class="image">
                <img src="{{ post.image | relative_url }}" alt="" data-position="center center" />
            </a>
            <div class="content">
                <div class="inner">
                    <header class="major">
                        <h3>{{ post.title }}</h3>
                    </header>
                    <p><strong>Stars：</strong>{{ post.rating }}</p>
                    <p>{{ post.description }}</p>
                    <ul class="actions">
                        <li><a href="{{ post.url | relative_url }}" class="button">阅读全文</a></li>
                    </ul>
                </div>
            </div>
        </section>
        {% endfor %}
    </section>
</div>
