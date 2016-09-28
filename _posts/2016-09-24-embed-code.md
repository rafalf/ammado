---
layout: post
title:  "embed code"
date:   2016-09-24
desc: "embed code"
keywords: "test, widgets"
categories: [Test]
tags: [test, widgets, all]
published: false
---

___


<input id="testCode" type="text" style="height:200px; font-size:14pt; width:100%; text-align: center;" value="please enter the code here" onfocus="if(this.value == 'please enter the code here') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'please enter the code here'; }">

<div class="text-center article-title">
<h2>
<input id="submit" type="submit" value="Submit" onClick="submitForm()">
</h2>
</div>


<div id="innerHtml"> 
</div>


 <script>
         
    function submitForm() {
    
         var testCode = document.getElementById('testCode').value;
         console.log(testCode);	

         //document.getElementById('innerHtml').innerHTML = testCode;

        }

 </script>