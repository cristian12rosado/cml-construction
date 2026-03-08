<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<header class="site-header">
  <div class="container nav">
    <div class="brand">
      <div class="brand-mark">▦</div>
      <div class="brand-text">
        <span>CIVIL</span>
        <span>ENGINEERING</span>
      </div>
    </div>

    <nav class="desktop-nav">
      <a href="#home">{t.nav.home}</a>
      <a href="#services">{t.nav.services}</a>
      <a href="#projects">{t.nav.projects}</a>
      <a href="#about">{t.nav.about}</a>
      <a href="#contact">{t.nav.contact}</a>
    </nav>

    <div class="lang-switch">
      <button class:active={$language === 'en'} on:click={() => language.set('en')}>EN</button>
      <button class:active={$language === 'es'} on:click={() => language.set('es')}>ES</button>
    </div>
  </div>
</header>