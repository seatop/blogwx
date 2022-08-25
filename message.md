---
layout: default
title: Message
nav_order: 5
nav_exclude: true
permalink: /message.html
---

## @
{: .m-5 }

<p id="say"></p>
{: .fs-6 .fw-300 .m-5 .p-5 }

<script>
function GetQueryString(name) {
var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)","i");
var r = window.location.search.substr(1).match(reg);
if (r!=null) return (r[2]); return "无消息";
}
document.getElementById("say").innerHTML = decodeURIComponent(GetQueryString("s"));
</script>