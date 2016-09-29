---
layout: post
title:  "test - ammado fundraising widget"
date:   2016-09-25
desc: "fundraising widget test site"
keywords: "test, fundraising widget"
categories: [Test]
tags: [test, fundraising widget]
published: true
---


<div class="pull-right">
<button onclick="location.href='{{"/configuration"| prepend: site.baseurl }}'" class="btn btn-white btn-xs" type="button">Configuration</button>
</div>
___

<form name="myform" action="{{"/fundraise/" | prepend: site.baseurl }}" method="GET">
<table style="width:40%; " align="center" cellpadding="10">
<tr>
<td><strong>test site: </strong>www.</td>
<td><input id="testUrl" type="text" name="testUrl" value="ammado.com"></td>
</tr>
<tr>
<td><strong>entity type: </strong></td>
<td><input id="entityType" type="text" name="entityType" value="nonprofit"></td>
</tr>
<tr>
<td><strong>entity id (address profile):</strong></td>
<td><input id="entityID" type="text" name="entityID" value="ifrc"></td>
</tr>
<tr>
<td><strong>campaign id:</strong></td>
<td><input id="campID" type="text" name="campID" value=""></td>
</tr>

</table>

<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit">

</h2>
</div>

</form>