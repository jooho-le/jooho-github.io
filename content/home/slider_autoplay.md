---
widget: blank
headless: true
weight: 12
title: ''
---

<script>
  // Auto-advance Home slider every 6 seconds
  (function () {
    function nextSlide() {
      var nextBtn = document.querySelector('.wg-slider .carousel-control-next');
      if (nextBtn) nextBtn.click();
    }
    // Start after DOM is ready
    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', function(){ setInterval(nextSlide, 6000); });
    } else {
      setInterval(nextSlide, 6000);
    }
  })();
</script>

