---
title: Contact
date: 2016-10-16 12:08:00 +02:00
horaires: |+
  Lundi au vendredi de 09h00 à 12h15 et de 13h30 à 19h00
  Samedi de 09h00 à 12h15 et de 13h30 à 15h00
  Fermé le jeudi ou sur rendez vous.

---

<style>
dl.inline dd {
  display: inline; 
  margin: 0;
}
dl.inline dd:after{ 
  display: block;  
  content: '';
}
dl.inline dt{
  margin: 5px;
  display: inline-block;
  text-align: right;  
  min-width: 25px;  
}
</style>

<dl class="inline">
  <dt><span class="octicon octicon-location"></span></dt>
  <dd>{{site.address.line1}}</dd>
  <dt></dt> 
  <dd>{{site.address.line2}}</dd>  
  <dt>Tel.</dt>
  <dd>{{site.phone}}</dd>  
  <dt><span class="octicon octicon-device-mobile"></span></dt>
  <dd>{{site.mobile}}</dd>  
  <dt>Fax.</dt>
  <dd>{{site.fax}}</dd>  
  <dt><span class="octicon octicon-mail"></span></dt>
  <dd>{{site.email}}</dd>  
</dl>