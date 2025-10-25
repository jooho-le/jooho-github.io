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
    function advanceWithClasses(el, dir){
      var items = el.querySelectorAll('.carousel-item');
      if (!items.length) return;
      var active = el.querySelector('.carousel-item.active') || items[0];
      var i = Array.prototype.indexOf.call(items, active);
      var nextIndex = (i + (dir > 0 ? 1 : -1) + items.length) % items.length;
      if (active) active.classList.remove('active');
      items[nextIndex].classList.add('active');
    }

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
        setInterval(function(){ advanceWithClasses(el, +1); }, 6000);
        if (nextCtrl) nextCtrl.addEventListener('click', function(e){ e.preventDefault(); advanceWithClasses(el, +1); });
        if (prevCtrl) prevCtrl.addEventListener('click', function(e){ e.preventDefault(); advanceWithClasses(el, -1); });
      }
    }

    // Event delegation in case controls are re-rendered later
    document.addEventListener('click', function(e){
      var next = e.target.closest('.wg-slider .carousel-control-next');
      var prev = e.target.closest('.wg-slider .carousel-control-prev');
      if (!next && !prev) return;
      var el = document.querySelector('.wg-slider .carousel');
      if (!el) return;
      e.preventDefault();
      if (window.bootstrap && window.bootstrap.Carousel) {
        var instance = window.bootstrap.Carousel.getOrCreateInstance(el);
        if (next) instance.next(); else instance.prev();
      } else {
        advanceWithClasses(el, next ? +1 : -1);
      }
    }, true);

    function waitForCarousel(){
      var el = document.querySelector('.wg-slider .carousel');
      if (el) { initCarousel(el); return; }
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

