---
widget: blank
headless: true
weight: 12
title: ''
---

<script>
  // Robust slider control: wait for the carousel to exist, then
  // initialize Bootstrap's Carousel API and wire arrow controls.
  (function () {
    function initCarousel(el){
      if (!el) return;
      // Fix odd hashes on controls to avoid errors
      var nextCtrl = el.querySelector('.carousel-control-next');
      var prevCtrl = el.querySelector('.carousel-control-prev');
      if (nextCtrl && (!nextCtrl.getAttribute('href') || nextCtrl.getAttribute('href') === '#.')) nextCtrl.setAttribute('href', '#');
      if (prevCtrl && (!prevCtrl.getAttribute('href') || prevCtrl.getAttribute('href') === '#.')) prevCtrl.setAttribute('href', '#');

      if (window.bootstrap && window.bootstrap.Carousel) {
        var instance = window.bootstrap.Carousel.getOrCreateInstance(el, {
          interval: 6000,   // auto interval
          ride: false,
          pause: false,
          wrap: true,
          touch: true
        });
        // Ensure arrows control via API and don't navigate the hash
        if (nextCtrl) nextCtrl.addEventListener('click', function(e){ e.preventDefault(); instance.next(); });
        if (prevCtrl) prevCtrl.addEventListener('click', function(e){ e.preventDefault(); instance.prev(); });
      } else {
        // Fallback: manual cycle with classes
        setInterval(function(){
          var items = el.querySelectorAll('.carousel-item');
          if (!items.length) return;
          var active = el.querySelector('.carousel-item.active');
          var i = Array.prototype.indexOf.call(items, active);
          var nextIndex = (i + 1) % items.length;
          if (active) active.classList.remove('active');
          items[nextIndex].classList.add('active');
        }, 6000);
        if (nextCtrl) nextCtrl.addEventListener('click', function(e){ e.preventDefault(); var act=el.querySelector('.carousel-item.active'); var items=el.querySelectorAll('.carousel-item'); var i=Array.prototype.indexOf.call(items, act); var n=(i+1)%items.length; if(act) act.classList.remove('active'); items[n].classList.add('active'); });
        if (prevCtrl) prevCtrl.addEventListener('click', function(e){ e.preventDefault(); var act=el.querySelector('.carousel-item.active'); var items=el.querySelectorAll('.carousel-item'); var i=Array.prototype.indexOf.call(items, act); var p=(i-1+items.length)%items.length; if(act) act.classList.remove('active'); items[p].classList.add('active'); });
      }
    }

    function waitForCarousel(){
      var el = document.querySelector('.wg-slider .carousel');
      if (el) { initCarousel(el); return; }
      // poll up to 5 seconds as the theme may hydrate after DOM ready
      var tries = 0;
      var t = setInterval(function(){
        tries++;
        var el2 = document.querySelector('.wg-slider .carousel');
        if (el2){ clearInterval(t); initCarousel(el2); }
        if (tries > 50) clearInterval(t);
      }, 100);
    }

    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', waitForCarousel);
    } else {
      waitForCarousel();
    }
  })();
</script>
