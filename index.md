---
layout: default
title: 首页
---

<div class="post-list">
  <h2 style="margin-bottom: 25px; color: #4a9eff;">📚 最新发布</h2>
  
  {% for post in site.posts limit: 10 %}
  <div class="post-item">
    <h3 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <div class="post-meta">
      📅 {{ post.date | date: "%Y年%m月%d日" }}
      {% if post.tags %}
      · 
      {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
      {% endif %}
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncate: 150 }}
    </div>
  </div>
  {% endfor %}
</div>

<div class="highlight-box" style="text-align: center; margin-top: 40px;">
  <h3 style="color: #4a9eff; margin-bottom: 15px;">🌟 正在连载</h3>
  <p style="font-size: 1.1em; margin-bottom: 20px;">
    <strong>《午夜酒店》</strong> - 长篇悬疑连载
  </p>
  <p style="color: #aaa; margin-bottom: 20px;">
    一家只在凌晨 2 点 -5 点营业的神秘酒店<br>
    每条规则背后都藏着秘密
  </p>
  <a href="/fiction/midnight-hotel/" style="display: inline-block; background: linear-gradient(135deg, #4a9eff 0%, #9b59b6 100%); color: white; padding: 12px 30px; border-radius: 25px; font-weight: bold;">开始阅读 →</a>
</div>
