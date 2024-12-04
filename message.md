---
layout: default
title: Message
---

<div class="posts">
	<div class="post">
	  {% include author.html %}
	  <div class="content">
         <p class="ctitle" id="ctitle"></p>
         <div id="ctext"></div>
	  </div>
	</div>
</div>

<script>
	let u = new URL(document.URL);
	document.getElementById('ctitle').innerHTML = u.searchParams.get('t')?u.searchParams.get('t'):'@';
	document.getElementById('ctext').innerHTML = u.searchParams.get('c')?u.searchParams.get('c'):'：)';
</script>