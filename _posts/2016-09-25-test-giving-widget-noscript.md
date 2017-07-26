---
layout: post
title:  "test - ammado giving widget no frame"
date:   2016-09-25
desc: "giving widget customization"
keywords: "test, wigdet no frame"
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
<td><strong>entity type: </strong></td>
<td><input id="entityType" type="text" name="testUrl" value="company" onfocus="if(this.value == 'company') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'company'; }"></td>
</tr>

<tr>
<td><strong>entity id: </strong></td>
<td><input id="entityId" type="text" name="testUrl" value="586" onfocus="if(this.value == '586') { this.value = ''; }" onblur="if(this.value == '') { this.value = '586'; }"></td>
</tr>

<tr>
<td><strong>width:</strong></td>
<td><input id="gfwidth" type="text" name="gfwidth" value="320"  onfocus="if(this.value == '320') { this.value = ''; }" onblur="if(this.value == '') { this.value = '320'; }"></td>
</tr>
<tr>
<td><strong>height</strong></td>
<td><input id="gfheight" type="text" name="gfheight" value="436" onfocus="if(this.value == '436') { this.value = ''; }" onblur="if(this.value == '') { this.value = '436'; }"></td>
</tr>
<!--
<tr>
<td><strong>partner code</strong></td>
<td><input id="pcode" type="text" name="pcode" value=""></td>
</tr>
-->
</table>


<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit" style="font-family: Cursive;" onClick="loadFrame()">
</h2>
</div>

___

<div style="-webkit-overflow-scrolling:touch;"><iframe id="giving" src="about:blank" width="0" height="0" frameborder="0" marginwidth="0" marginheight="0" hspace="0" vspace="0" style="border: 1px solid #dadada;"></iframe></div>

<!--example-->
<!--<div style="-webkit-overflow-scrolling:touch;"><iframe src="https://www.ammadonightly4.com/company/586/givingwidget" width="320" height="436" frameborder="0" marginwidth="0" marginheight="0" hspace="0" vspace="0" style="border: 1px solid #dadada;"></iframe></div>-->


 <script>
         
function loadFrame() {

     var wwwSite = "https://www."
     var urlSite = document.getElementById('testUrl').value;
//     var pcode = document.getElementById('pcode').value;

//   example: company/586/givingwidget
     var entityId = document.getElementById('entityId').value;
     var entityType = document.getElementById('entityType').value;
     var fullurlSite = wwwSite.concat(urlSite, '/', entityType, '/', entityId, '/givingwidget')

     var gfwidth = document.getElementById('gfwidth').value;
     var gfheight = document.getElementById('gfheight').value;

     console.log(fullurlSite, gfwidth, gfheight);	

     document.getElementById('giving').src = fullurlSite;
     document.getElementById('giving').width = gfwidth;
     document.getElementById('giving').height = gfheight;

     alert('iFrame update:\nsite: ' + urlSite + '\nwidth: ' + gfwidth + '\nheight: ' + gfheight);

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