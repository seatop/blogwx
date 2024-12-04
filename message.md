---
layout: default
title: Message
---

<div class="posts">
	<div class="post">
	  {% include author.html %}
	  <div class="content">
         <p class="ctitle"></p>
         <div class="ctext"></div>
	  </div>
	</div>
</div>

<script>
	let u = new URL(document.URL);
	let title = u.searchParams.get('t');
	let content = u.searchParams.get('c');
	document.getElementsByClassName('ctitle').innerHTML = title;
	document.getElementsByClassName('ctext').innerHTML = content;

</script>