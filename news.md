---
layout: default
title: News
nav_order: 5
nav_exclude: true
permalink: /news.html
---

<p id="ntitle"></p>
{: .fs-7 .fw-400 .m }

<p id="say"></p>
{: .fs-6 .fw-300 .m-5 }

<script>
function GetQueryString(name) {
var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)","i");
var r = window.location.search.substr(1).match(reg);
if (r!=null) return (r[2]); return "未定义";
}
document.getElementById("ntitle").innerHTML = decodeURIComponent(GetQueryString("t"));
document.getElementById("say").innerHTML = decodeURIComponent(GetQueryString("s"));
</script>