<div class="hero-section">
  <h1 class="animated-title">Welcome</h1>
  <div class="profile-container">
    <img src="images/homepage_profpic.jpg" class="profile-image" alt="Profile picture">
  </div>
  <p class="animated-text">Hi! You found my website! I haven't added much yet, but please stay tuned, the seeds are still germinating. Next week I will plant them, and after that there will be a lot of watering!</p>
</div>

<div class="interactive-section">
  <h2 class="glowing-text">Master in Design for Emergent Futures</h2>
  <div class="floating-elements">
    <div class="floating-circle circle-1"></div>
    <div class="floating-circle circle-2"></div>
    <div class="floating-circle circle-3"></div>
  </div>
</div>

<!-- Floating Clock Widgets -->
<div class="clock-widgets">
  <div class="clock-container barcelona-clock">
    <div class="clock-widget">
      <div class="clock-header">Barcelona</div>
      <div class="clock-time" id="barcelona-time">--:--</div>
      <div class="clock-date" id="barcelona-date">--</div>
    </div>
  </div>
  
  <div class="clock-container montreal-clock">
    <div class="clock-widget">
      <div class="clock-header">Montreal</div>
      <div class="clock-time" id="montreal-time">--:--</div>
      <div class="clock-date" id="montreal-date">--</div>
    </div>
  </div>
  
  <div class="clock-container sanfrancisco-clock">
    <div class="clock-widget">
      <div class="clock-header">San Francisco</div>
      <div class="clock-time" id="sanfrancisco-time">--:--</div>
      <div class="clock-date" id="sanfrancisco-date">--</div>
    </div>
  </div>
</div>

<script>
// Clock functionality
function updateClocks() {
  const now = new Date();
  
  // Barcelona time (CET/CEST)
  const barcelonaTime = new Date(now.toLocaleString("en-US", {timeZone: "Europe/Madrid"}));
  document.getElementById('barcelona-time').textContent = barcelonaTime.toLocaleTimeString('en-US', {hour12: false, hour: '2-digit', minute: '2-digit'});
  document.getElementById('barcelona-date').textContent = barcelonaTime.toLocaleDateString('en-US', {weekday: 'short', month: 'short', day: 'numeric'});
  
  // Montreal time (EST/EDT)
  const montrealTime = new Date(now.toLocaleString("en-US", {timeZone: "America/Montreal"}));
  document.getElementById('montreal-time').textContent = montrealTime.toLocaleTimeString('en-US', {hour12: false, hour: '2-digit', minute: '2-digit'});
  document.getElementById('montreal-date').textContent = montrealTime.toLocaleDateString('en-US', {weekday: 'short', month: 'short', day: 'numeric'});
  
  // San Francisco time (PST/PDT)
  const sanfranciscoTime = new Date(now.toLocaleString("en-US", {timeZone: "America/Los_Angeles"}));
  document.getElementById('sanfrancisco-time').textContent = sanfranciscoTime.toLocaleTimeString('en-US', {hour12: false, hour: '2-digit', minute: '2-digit'});
  document.getElementById('sanfrancisco-date').textContent = sanfranciscoTime.toLocaleDateString('en-US', {weekday: 'short', month: 'short', day: 'numeric'});
}

// Update clocks immediately and then every second
updateClocks();
setInterval(updateClocks, 1000);
</script> 
