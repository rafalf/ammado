---
layout: post
title:  "site configuration"
date:   2016-09-27
desc: "eggs for food site configuration"
keywords: "test"
categories: [Test]
tags: [test, donations, widgets, config, cookies]
published: true
permalink: /configuration/
---

# test accounts: data populator

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany6')">Remember me</button>
</div>

__acompany6:__

giving widget whitelist: 6

giving widget skin name: burgundy

---

---
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany8')">Remember me</button>
</div>

__acompany8:__

giving widget whitelist: 22

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany10')">Remember me</button>
</div>

__acompany10:__

giving widget whitelist: France, All categories

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany12')">Remember me</button>
</div>

__acompany12:__

partner code: pcTest

___


# test site

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('www','ammadonightly1.com', 7)">Remember me</button>
</div>

www.ammadonightly1.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('www','ammadonightly2.com', 7)">Remember me</button>
</div>

www.ammadonightly2.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('www','ammadonightly3.com', 7)">Remember me</button>
</div>

www.ammadonightly3.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('www','ammadonightly4.com', 7)">Remember me</button>
</div>

www.ammadonightly4.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('www','ammado.com', 7)">Remember me</button>
</div>

www.ammado.com

---




<script>

function createCookies(entype, entid){
    createCookie('entype', entype, 7)
    createCookie('entid', entid, 7)
    }
    
function createCookie(name,value,days) {
	if (days) {
		var date = new Date();
		date.setTime(date.getTime()+(days*24*60*60*1000));
		var expires = "; expires="+date.toGMTString();
	}
	else var expires = "";
	document.cookie = name+"="+value+expires+"; path=/";
}

</script>



