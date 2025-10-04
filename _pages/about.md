---
permalink: /
title: "Welcome!"
excerpt: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-0N02QYVJTL"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-0N02QYVJTL');
</script>

Hi! I am Kah Hong! I am a ML-focused Quantitative Researcher based in Singapore, currently leading a small research team applying deep learning and statistical methods to Cryptocurrency HFT/CTA strategies. I was previously a Macro Quantitative Researcher in Geneva, Switzerland and Data Scientist in London, UK. I am interested in probabilistics modelling, machine learning and analytical solutions to inference problems in consumer technology, social phenomena, and the financial markets. I gravitate towards developing solutions with long-term stability and reliability in mind, and learn by breaking down problems and understanding technical concepts from first principles.

<div style="display: flex; gap: 20px; max-width: 1200px; margin: 20px auto;">
  <!-- Left Column -->
  <div style="flex: 1; display: flex; flex-direction: column; gap: 20px;">
    <div style="text-align: center;">
      <img src="/images/taipei1.jpeg" style="width: 100%; height: auto; border-radius: 8px;" loading="eager" alt="Taipei 101" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">From 71th Floor of Taipei 101, Taiwan, 2025</p>
    </div>
    <div style="text-align: center;">
      <img src="/images/highline_newyork.jpeg" style="width: 100%; height: auto; border-radius: 8px;" loading="eager" alt="High Line NYC" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Strolling along the High Line, New York, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/times_square.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Times Square" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Times Square, New York, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/newyork2.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Brooklyn Bridge" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Brooklyn Bridge, New York, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/cefalu2.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Cefalù Beach" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Spiaggia di Cefalù, Sicily, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/sicily.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Hiking Cefalù" />
      <p style="margin: 8px 0 0 0  
: 14px;">Hiking in Cefalù, Italy, 2022</p>
    </div>
  </div>
  
  <!-- Right Column -->
  <div style="flex: 1; display: flex; flex-direction: column; gap: 20px;">
    <div style="text-align: center;">
      <img src="/images/taipei2.jpeg" style="width: 100%; height: auto; border-radius: 8px;" loading="eager" alt="Taipei Park" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Zhong Shan Park, Taipei, 2025</p>
    </div>
     <div style="text-align: center;">
      <img src="/images/ig_newyork.jpeg" style="width: 100%; height: auto; border-radius: 8px;" loading="eager" alt="Instagram HQ" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Instagram New York Headquarters, USA, 2022</p>
    </div>
    <div style="text-align:中心;">
      <img data-src="/images/cefalu3.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Cefalù Beach 2" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Spiaggia di Cefalù, Sicily, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/catania2.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Catania" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Via degli Ombrellini in Catania, Sicily, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/syracuse.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Syracuse" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Island of Ortigia near Syracuse, Sicily, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/taormina.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Taormina" />
      <p style="margin: 14px;">Isola Bella in Taormina, Sicily, 2022</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/kognisee.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="Königssee Lake" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Lake Königssee, Germany, 2019</p>
    </div>
    <div style="text-align: center;">
      <img data-src="/images/sanfrancisco.jpeg" style="width: 100%; height: auto; border-radius: 8px;" class="lazy-img" alt="San Francisco" />
      <p style="margin: 8px 0 0 0; font-size: 14px;">Golden Gate Bridge in San Francisco, USA, 2022</p>
    </div>    
  </div>
</div>

<script>
// Progressive loading strategy
if ('IntersectionObserver' in window) {
  const imageObserver = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const img = entry.target;
        img.src = img.dataset.src;
        img.classList.remove('lazy-img');
        imageObserver.unobserve(img);
      }
    });
  }, {
    // Load images when they're 200px away from viewport
    rootMargin: '200px 0px',
    threshold: 0.1
  });

  // Only observe lazy images (skip eager loading ones)
  document.querySelectorAll('.lazy-img').forEach(img => {
    imageObserver.observe(img);
  });
}
</script>

<style>
.lazy-img {
opacity: 0;
transition: opacity 0.3s ease-in-out;
}

.lazy-img.loaded {
opacity: 1;
}

</style>

Hope you have enjoyed my personal feed.
