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

Click on 'Remember me' to store the entity data: entity type, entity id or profile address (identifier). Next time you get to the test form you'll have the input fields populated with these values.

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

giving widget whitelist: 22 (ac110 delisted)

giving widget skin name: burnt-umber

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany10')">Remember me</button>
</div>

__acompany10:__

giving widget whitelist: France, All categories

giving widget skin name: graphite-gray

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookies('company','acompany12')">Remember me</button>
</div>

__acompany12:__

partner code: pcTest

___


# test sites

Click on 'Set this site' to set the site for testing. 
It'll be overriden if you enter a different site name on the form.  

___
<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('testUrl','ammadonightly1.com', 7)">Set this site</button>
</div>

www.ammadonightly1.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('testUrl','ammadonightly2.com', 7)">Set this site</button>
</div>

www.ammadonightly2.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('testUrl','ammadonightly3.com', 7)">Set this site</button>
</div>

www.ammadonightly3.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('testUrl','ammadonightly4.com', 7)">Set this site</button>
</div>

www.ammadonightly4.com

---

<div class="pull-right">
<button class="btn btn-white btn-xs" type="button" onClick="createCookie('testUrl','ammado.com', 7)">Set this site</button>
</div>

www.ammado.com

---




<script>

function createCookies(entype, entid){
    createCookie('entityType', entype, 7)
    createCookie('entityID', entid, 7)
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



