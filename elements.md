---
layout: page
title: Journal
description: My Journal
background: assets/images/pic02.jpg
---

<div id="main" class="alt">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Welcome!</h1>
            </header>

            <ul class="alt">
                {% for post in site.posts %}
                <li>
                    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
                    <p>{{ post.date | date: "%B %d, %Y" }} - {{ post.description }}</p>
                </li>
                {% endfor %}
            </ul>
            
        </div>
    </section>
</div>
