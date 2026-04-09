---
layout: default
title: 悬疑小说
---

<h2 style="margin-bottom: 25px; color: #4a9eff;">🔍 悬疑小说</h2>

<div class="highlight-box" style="text-align: center; margin-bottom: 40px;">
  <h3 style="color: #4a9eff; margin-bottom: 10px;">🏨 正在连载</h3>
  <p style="font-size: 1.2em; margin-bottom: 10px;"><strong>《午夜酒店》</strong></p>
  <p style="color: #aaa;">一家只在凌晨 2 点 -5 点营业的神秘酒店<br>每条规则背后都藏着秘密</p>
</div>

<h3 style="color: #eaeaea; margin-bottom: 20px;">📖 午夜酒店 · 章节列表</h3>

<div class="post-list">
  {% assign sorted = site.posts | where_exp: "p", "p.tags contains '午夜酒店'" | sort: "date" | reverse %}
  {% for post in sorted %}
  <div class="post-item">
    <h3 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <div class="post-meta">
      📅 {{ post.date | date: "%Y年%m月%d日" }}
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncate: 100 }}
    </div>
  </div>
  {% endfor %}
</div>

<h3 style="color: #eaeaea; margin: 40px 0 20px 0;">✍️ 短篇故事</h3>

<div class="post-list">
  {% assign shorts = site.posts | where_exp: "p", "p.tags contains '悬疑' and p.tags contains '短篇'" %}
  {% if shorts.size > 0 %}
    {% for post in shorts %}
    <div class="post-item">
      <h3 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <div class="post-meta">
        📅 {{ post.date | date: "%Y年%m月%d日" }}
      </div>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncate: 100 }}
      </div>
    </div>
    {% endfor %}
  {% else %}
    {% for post in site.posts %}
      {% unless post.tags contains '午夜酒店' or post.tags contains '思维趣题' or post.tags contains '每日更新' %}
        {% if post.title != '关于星期天书房' and post.title != '欢迎来到星期天书房' %}
        <div class="post-item">
          <h3 class="post-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <div class="post-meta">
            📅 {{ post.date | date: "%Y年%m月%d日" }}
          </div>
          <div class="post-excerpt">
            {{ post.excerpt | strip_html | truncate: 100 }}
          </div>
        </div>
        {% endif %}
      {% endunless %}
    {% endfor %}
  {% endif %}
</div>
