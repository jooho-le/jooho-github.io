---
widget: blank
headless: true
weight: 12
title: ''
---

<script>
  // Auto-advance the Home slider without clicking the Next anchor
  // (Clicking the anchor updates the URL hash and can cause the page to jump to the slider.)
  (function () {
    function startCarouselAutoplay() {
      var el = document.querySelector('.wg-slider .carousel');
      if (!el) return;

      // Prefer Bootstrap's Carousel API to avoid hash/scroll changes
      if (window.bootstrap && window.bootstrap.Carousel) {
        var instance = window.bootstrap.Carousel.getOrCreateInstance(el, {
          interval: false, // we'll drive it manually
          ride: false,
          pause: false,
          wrap: true
        });
        setInterval(function(){ instance.next(); }, 6000);
      } else {
        // Fallback: switch active slide with classes (no anchor clicks)
        setInterval(function(){
          var items = el.querySelectorAll('.carousel-item');
          if (!items.length) return;
          var active = el.querySelector('.carousel-item.active');
          var i = Array.prototype.indexOf.call(items, active);
          var nextIndex = (i + 1) % items.length;
          if (active) active.classList.remove('active');
          items[nextIndex].classList.add('active');
        }, 6000);
      }
    }

    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', startCarouselAutoplay);
    } else {
      startCarouselAutoplay();
    }
  })();
</script>
