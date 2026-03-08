<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<section id="home" class="hero">
  <div class="hero-overlay"></div>
  <img
    class="hero-image"
    src="https://images.unsplash.com/photo-1513828583688-c52646db42da?auto=format&fit=crop&w=1800&q=80"
    alt="Civil engineering bridge project"
  />

  <div class="container hero-content">
    <p class="eyebrow">{t.hero.eyebrow}</p>
    <h1>{t.hero.titleTop}<br />{t.hero.titleBottom}</h1>
    <p class="hero-copy">{t.hero.description}</p>

    <div class="hero-actions">
      <a href="#projects" class="btn btn-primary">{t.hero.primary}</a>
      <a href="#contact" class="btn btn-outline">{t.hero.secondary}</a>
    </div>
  </div>
</section>