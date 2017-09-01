---
layout: post
title:  "test - ammado donation widget btn placement"
date:   2016-09-25
desc: "placement widget"
keywords: "test, donation widget, placement"
categories: [Test]
tags: [test, donation, button]
published: true
---

___

<div class="text-center article-title">
<h2>Choose your configuration</h2>
</div>

<div class="pull-right">
<button onclick="location.href='{{"/configuration"| prepend: site.baseurl }}'" class="btn btn-white btn-xs" type="button">Set default configuration</button>
</div>


<table style="width:40%; font-size: 16px;" align="center" cellpadding="10" >
<tr>
<td><strong>test site: </strong>www.</td>
<td><input id="testUrl" type="text" name="testUrl" value="ammadonightly4.com" onfocus="if(this.value == 'ammadonightly4.com') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ammadonightly4.com'; }"></td>
</tr>

<tr>
<td><strong>fundraiser id: </strong></td>
<td><input id="fundriaserID" type="text" name="fundriaserID" value="965" onfocus="if(this.value == '965') { this.value = ''; }" onblur="if(this.value == '') { this.value = '965'; }"></td>
</tr>

<tr>
<td><strong>placement: </strong></td>
<td><input id="placement" type="text" name="placement" value="www.digitalliveaid.org" onfocus="if(this.value == 'www.digitalliveaid.org') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'www.digitalliveaid.org'; }"></td>
</tr>

</table>


<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit" style="font-family: Cursive;" onClick="loadButton()">
</h2>
</div>

___
    
<div id="ammadoCustomButton">
<a class="donateButton" id="placementBtn" href="https://www.ammadonightly4.com/donate?1331&placementUrl=www.digitalliveaid.org" target="_blank">Submitted? then click on Donate btn ==>
<img id="ammadoDonateButton" border="0" src="https://github.com/rafalf/ammado/blob/master/static/img/blog/donate_322.png?raw=true" width="150" height="100" data-original-width="300" data-original-height="250" />
</a>
</div>


<style type="text/css">
.overlay, .overlay-content {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0
}

.overlay {
    z-index: 500;
    background-color: #000;
    opacity: .8;
    padding: 5px 0
}

.overlay-content {
    margin: auto;
    -moz-border-radius: 5px;
    -webkit-border-radius: 5px;
    border-radius: 5px;
    z-index: 501;
    background: #fff url("../images/loading.gif") no-repeat center;
    background-size: 48px 48px;
    width: 600px;
    height: 600px
}

.overlay-content iframe {
    width: 100%;
    height: 100%;
    -moz-border-radius: 5px;
    -webkit-border-radius: 5px;
    border-radius: 5px;
    padding: 0
}

.closeOverlay {
    color: #2e2e2e;
    padding: 3px 5px;
    background-color: #fff;
    opacity: .9;
    cursor: pointer;
    position: absolute;
    right: 9px;
    top: -12px;
    -moz-border-radius: 50px;
    -webkit-border-radius: 50px;
    border-radius: 50px;
    border: 2px solid #6dc46b
}

.closeOverlay:hover {
    opacity: 1
}
</style>


<script src="{{"/static/js/siteJs.min.js"| prepend: site.baseurl }}"></script>
  
 <script>
 
	$(document).ready(function () {
		dla.initDonateLinks($('body'));
	});
   
function loadButton() {
    
     <!--https://www.ammadodemo.com/donate?1331&placementUrl=www.digitalliveaid.org -->
     
     var wwwSite = "https://www."
     var urlSite = document.getElementById('testUrl').value;
     var fundriaserID = document.getElementById('fundriaserID').value;
     var placement = document.getElementById('placement').value;
     var fullurlSite = wwwSite.concat(urlSite, '/donate?', fundriaserID, '&placementUrl=',placement)

     console.log(fullurlSite);	

     document.getElementById('placementBtn').href = fullurlSite;

     alert('Button href update:\nsite: ' + urlSite + '\nfundraiser id: ' + fundriaserID + '\nplacement: ' + placement + 
            '\nhref: ' + fullurlSite);

     // set www cookie
     createCookie('www', urlSite, 7);
     console.log('www cookie set: ' + urlSite);

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