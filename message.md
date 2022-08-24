---
layout: default
title: message
nav_order: 5
nav_exclude: true
permalink: /message.html
---

### @

<p id="say"></p>
{: .fs-6 .fw-300 }

<script>
function GetQueryString(name) {
var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)","i");
var r = window.location.search.substr(1).match(reg);
if (r!=null) return (r[2]); return "无消息";
}
document.getElementById("say").innerHTML = decodeURIComponent(GetQueryString("s"));
</script>