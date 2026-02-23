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
                <h1>Reviews / 书影音</h1>
            </header>
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
                    <div class="rating" style="color: #f39c12; margin-bottom: 1em;">
                        Rating：{{ post.rating }}
                    </div>
                </header>
                <p>{{ post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ post.url | relative_url }}" class="button">Read full</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endfor %}
</section>
</div>
