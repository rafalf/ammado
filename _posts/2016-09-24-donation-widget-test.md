---
layout: post
title:  "ammado donation widget v.1 - test"
date:   2016-09-24
desc: "donation widget"
keywords: "live, donation widget"
categories: [Test]
tags: [test, donation widget]
published: true
---

### ammado donation widget v.1 - test

___

<form name="myform" action="{{"/donate/" | prepend: site.baseurl }}" method="GET">
<table style="width:40%; " align="center" cellpadding="10">
<tr>
<td><strong>test site: </strong>www.</td>
<td><input id="testUrl" type="text" name="testUrl" value="ammado.com" onfocus="if(this.value == 'ammado.com') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ammado.com'; }"></td>
</tr>
<tr>
<td><strong>entity type: </strong></td>
<td><input id="entityType" type="text" name="entityType" value="nonprofit" onfocus="if(this.value == 'nonprofit') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'nonprofit'; }"></td>
</tr>
<tr>
<td><strong>entity id (address profile):</strong></td>
<td><input id="entityID" type="text" name="entityID" value="ifrc" onfocus="if(this.value == 'ifrc') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ifrc'; }"></td>
</tr>

</table>

<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit">

</h2>
</div>

</form>