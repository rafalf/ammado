---
layout: post
title:  "test - ammado donation widget v.1"
date:   2016-09-25
desc: "donation widget"
keywords: "test, donation widget"
categories: [Test]
tags: [test, donation widget]
published: true
---


<div class="pull-right">
<button onclick="location.href='{{"/configuration"| prepend: site.baseurl }}'" class="btn btn-white btn-xs" type="button">Configuration</button>
</div>
___

<br>

<div class="text-center article-title">
<h2>Step 1: Choose your configuration:</h2>
</div>

<table align="center">

<tr>
<td>
  <select style="font-size: 21px; border: 0;" name="selentity" id="selentity" onchange="fillformentity();">
    <option value="" selected>Please select ...</option>
    <option value="ifrccomp">ifrc company</option>
    <option value="testnonprofit">test nonprofit</option>
    <option value="testcompany">test company</option>
    <option value="">-----------------</option>
    <option value="acompany8">acompany8</option>
    <option value="acompany6">acompany6</option>
  </select>
</td>
</tr>
</table>

<br>

<table align="center">
<tr>
<td>
  <select style="font-size: 21px; border: 0;" name="selsite" id="selsite" onchange="fillformsite();">>
    <option value="" selected>Please select ...</option>
    <option value="ammadonightly4.com">ammadonightly4</option>
    <option value="ammadonightly3.com">ammadonightly3</option>
    <option value="ammadonightly2.com">ammadonightly2</option>
    <option value="ammadonightly1.com">ammadonightly1</option>
    <option value="qammado.com">qammado</option>
    <option value="ammado.com">ammado</option>
  </select>
</td>
</tr>
</table>

<br>

---
<div class="text-center article-title">
<h2>Step 2: Review your configuration:</h2>
</div>

<form name="myform" action="{{"/donate/" | prepend: site.baseurl }}" method="GET">
<table style="width:40%; font-size: 16px;" align="center" cellpadding="10" >
<tr>
<td>Test Site:</td>
<td><input id="testUrl" type="text" name="testUrl" value="ammado.com" onfocus="if(this.value == 'ammado.com') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ammado.com'; }"></td>
</tr>
<tr>
<td>Entity Type:</td>
<td><input id="entityType" type="text" name="entityType" value="nonprofit" onfocus="if(this.value == 'nonprofit') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'nonprofit'; }"></td>
</tr>
<tr>
<td>Entity Id:</td>
<td><input id="entityID" type="text" name="entityID" value="ifrc" onfocus="if(this.value == 'ifrc') { this.value = ''; }" onblur="if(this.value == '') { this.value = 'ifrc'; }"></td>
</tr>
</table>

<hr>

<div class="text-center article-title">
<h2>Step 3: Submit!</h2>
</div>

<div class="text-center article-title">
<h1>
<input id="submit" type="submit" value="Submit" style="font-family: Cursive;">
</h1>
</div>

</form>


<script>
function fillformentity(){
    var entityid = document.getElementById("selentity").value;
    if (entityid) {
        var entitydata = returntype(entityid);
        document.getElementById("entityType").value= entitydata[0];
        document.getElementById("entityID").value=entitydata[1];
        }
    }

function fillformsite(){
    var site = document.getElementById("selsite").value;
    document.getElementById("testUrl").value= site;
    }

function returntype(entityname){
    var arr = {
            "ifrccomp": ["company", "120482"],
            "testcompany": ["company","175962"],
            "testnonprofit":["nonprofit","147784"],
            "acompany6":["company","acompany6"],
            "acompany8":["company","acompany8"]
              };
    return arr[entityname];
    }
</script>


                                    