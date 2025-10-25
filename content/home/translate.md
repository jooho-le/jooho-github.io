---
widget: blank
headless: true
weight: 2
title: ''
---

<div id="google_translate_element" style="display:none"></div>
<style>
  .goog-te-banner-frame{display:none!important}
  .goog-logo-link, .goog-te-gadget{display:none!important}
  body{top:0!important}
  .skiptranslate{display:none!important}
</style>
<script>
  (function(){
    var lang = (document.documentElement.getAttribute('lang')||'').toLowerCase();
    if(!lang.startsWith('en')) return; // Only auto-translate when EN selected
    function googleTranslateElementInit(){
      try{ new google.translate.TranslateElement({pageLanguage:'ko', includedLanguages:'en', autoDisplay:false}, 'google_translate_element'); }catch(e){}
    }
    document.cookie = 'googtrans=/ko/en;path=/';
    document.cookie = 'googtrans=/ko/en;domain='+location.hostname+';path=/';
    var s=document.createElement('script');
    s.src='//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit';
    document.head.appendChild(s);
  })();
  </script>

