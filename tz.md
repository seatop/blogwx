---
layout: default
title: 教师节快乐
nav_order: 5
nav_exclude: true
permalink: /tz.html
---

![教师节题图](./images/teacher_h.png)

<p>祝<span id="tname"></span>老师节日快乐！</p>
{: .fs-6 .fw-400 .mx-auto }

<p>读万卷书，行万里路，感谢您的无私奉献，在这中秋遇上教师的节日里，请接受学生最美好的祝愿，亲爱的老师，祝您快乐!</p>
{: .fs-5 .fw-300 .m-5 }

![教师节图脚](./images/teacher_f.png)

<script>
function GetQueryString(name) {
var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)","i");
var r = window.location.search.substr(1).match(reg);
if (r!=null) return (r[2]); return "";
}
document.getElementById("tname").innerHTML = decodeURIComponent(GetQueryString("t"));
</script>