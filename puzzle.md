---
layout: default
title: 思维趣题
---

<h2 style="margin-bottom: 25px; color: #4a9eff;">🧩 每日思维趣题</h2>

<div class="highlight-box" style="text-align: center; margin-bottom: 40px;">
  <p style="font-size: 1.1em; margin-bottom: 10px;">每天一道原创思维题 · 让大脑保持活力</p>
  <p style="color: #aaa;">逻辑推理 · 思维陷阱 · 脑力训练</p>
</div>

<div class="post-list">
  {% assign puzzles = site.posts | where_exp: "p", "p.tags contains '思维趣题'" | sort: "date" | reverse %}
  {% for post in puzzles %}
  <div class="post-item">
    <h3 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <div class="post-meta">
      📅 {{ post.date | date: "%Y年%m月%d日" }}
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncate: 120 }}
    </div>
  </div>
  {% endfor %}
</div>
