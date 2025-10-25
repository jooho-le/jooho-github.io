---
widget: blank
headless: true
weight: 1
title: ''
---

<script>
  // Sanitize invalid carousel control attributes (e.g., href="#.")
  // and ensure controls point to the correct carousel to avoid errors like
  // "unrecognized expression: #." from vendor scripts.
  (function(){
    function fixControls() {
      try {
        var ctrls = document.querySelectorAll('a.carousel-control-next[href="#."], a.carousel-control-prev[href="#."]');
        ctrls.forEach(function(ctrl){
          // normalize href
          ctrl.setAttribute('href', '#');
          // resolve closest carousel and bind data-bs-target
          var car = ctrl.closest('.carousel');
          if (car) {
            if (!car.id) { car.id = 'home-carousel'; }
            ctrl.setAttribute('data-bs-target', '#'+car.id);
          }
        });
      } catch(e) { /* no-op */ }
    }
    // run immediately and observe future changes
    fixControls();
    var mo = new MutationObserver(function(){ fixControls(); });
    mo.observe(document.documentElement, {childList:true, subtree:true});
  })();
</script>

