---
layout: post
title:  "test - ammado purchase gift card widget"
date:   2016-09-25
desc: "gift card widget customization"
keywords: "test, gift card widget"
categories: [Test]
tags: [test, gift card widget]
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
<td><input id="testUrl" type="text" name="testUrl" value="ammado.com" onfocus="if(this.value == 'ammado.com') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ammado.com'; }"></td>
</tr>
<tr>
<td><strong>width:</strong></td>
<td><input id="gfwidth" type="text" name="gfwidth" value="360"  onfocus="if(this.value == '360') { this.value = ''; }" onblur="if(this.value == '') { this.value = '360'; }"></td>
</tr>
<tr>
<td><strong>height</strong></td>
<td><input id="gfheight" type="text" name="gfheight" value="580" onfocus="if(this.value == '580') { this.value = ''; }" onblur="if(this.value == '') { this.value = '580'; }"></td>
</tr>
<tr>
<td><strong>partner code</strong></td>
<td><input id="pcode" type="text" name="pcode" value=""></td>
</tr>
</table>


<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit" style="font-family: Cursive;" onClick="loadFrame()">
</h2>
</div>

___

<div style="text-align: center; margin: auto;"> 
<iframe id="giving" style="border: 1px solid #dddddd; margin: 0 auto" src="about:blank" width="360" height="620"></iframe>
</div>


 <script>
         
function loadFrame() {

     var wwwSite = "https://www."
     var urlSite = document.getElementById('testUrl').value;
     var pcode = document.getElementById('pcode').value;
     var fullurlSite = wwwSite.concat(urlSite, '/widget/buygiftcards', '?pc=', pcode)

     var gfwidth = document.getElementById('gfwidth').value;
     var gfheight = document.getElementById('gfheight').value;

     console.log(fullurlSite, gfwidth, gfheight);	

     document.getElementById('giving').src = fullurlSite;
     document.getElementById('giving').width = gfwidth;
     document.getElementById('giving').height = gfheight;

     alert('iFrame update:\nsite: ' + urlSite + '\nwidth: ' + gfwidth + '\nheight: ' + gfheight + '\npcode: ' + pcode);

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