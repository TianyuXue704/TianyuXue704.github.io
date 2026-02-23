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
                <h1>Journal / 随笔</h1>
            </header>
            
    <ul class="alt">
    {% for post in site.categories.diary %}
    <li>
        <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    </li>
    {% else %} <p>目前还没有日记。</p>
    {% endfor %}
</ul>
        </div>
    </section>
</div>>
