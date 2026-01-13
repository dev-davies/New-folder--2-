<script setup>
const personalInfo = {
  name: "DAVIES",
  tagline: "Clean code. Serious results.",
  intro: "I design and build clean, responsive web experiences where clarity comes first and complexity stays politely behind the curtain. Every pixel has a job, every interaction a purpose. This is a space for thoughtful front-end craftsmanship.",
  bio: "Hi — I'm Davies, a developer based in Nigeria. I specialise in building maintainable web apps with a focus on usability, accessibility, and a little personality. I’m a developer who enjoys turning ideas into digital products that don’t panic when they grow. I build projects with scale in mind from sleek landing pages that load fast and convert quietly, to full-blown web applications and ecommerce platforms designed to handle real users doing real things. My approach blends structure and curiosity. I care about clean architecture, reusable components, and interfaces that stay intuitive even as features multiply."
}
</script>

<template>
  <div class="app-container">
    <main class="container">
      <!-- Hero Section -->
      <section class="hero-section min-vh-100 d-flex align-items-center">
        <div class="row w-100 justify-content-center">
          <div class="col-lg-10">
            <h1 class="display-1 fw-black mb-4 tracking-tighter hero-title">
              {{ personalInfo.name }}
            </h1>
            <h2 class="h4 text-muted mb-5 fw-normal tracking-wide text-uppercase">
              {{ personalInfo.tagline }}
            </h2>
            <div class="row">
              <div class="col-md-9 col-lg-8">
                 <p class="lead hero-text mb-5">
                  {{ personalInfo.intro }}
                </p>
                <div class="d-flex gap-4">
                  <a href="#projects" class="custom-link">Selected Work</a>
                  <a href="#contact" class="custom-link">Get in Touch</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- About Section -->
      <section id="about" class="about-section py-large">
        <div class="row justify-content-center">
          <div class="col-lg-8">
            <span class="d-block text-muted font-monospace small mb-4">01 / ABOUT</span>
            <div class="about-content">
              <p class="mb-0">{{ personalInfo.bio }}</p>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
/* Typography Overrides */
.fw-black {
  font-weight: 900;
}

.tracking-tighter {
  letter-spacing: -0.05em;
}

.tracking-wide {
  letter-spacing: 0.1em;
}

.hero-title {
  font-size: clamp(5rem, 15vw, 12rem);
  line-height: 0.9;
  margin-left: -5px; /* Visual optical alignment */
}

.hero-text {
  font-size: 1.5rem;
  line-height: 1.6;
  font-weight: 300;
  color: var(--text-main);
}

.py-large {
  padding-top: 10rem;
  padding-bottom: 10rem;
}

.about-content p {
  font-size: 1.25rem;
  line-height: 1.8;
  color: var(--text-muted);
}

/* Custom Link Style */
.custom-link {
  position: relative;
  font-weight: 500;
  text-transform: uppercase;
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  padding-bottom: 2px;
  color: var(--text-main);
}

.custom-link::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 1px;
  background-color: var(--text-main);
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.3s ease;
}

.custom-link:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

/* Minimalist Utilities */
.min-vh-100 {
  min-height: 100vh;
}
</style>
