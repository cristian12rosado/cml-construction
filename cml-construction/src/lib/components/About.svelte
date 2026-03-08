<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<section id="about" class="section section-dark">
  <div class="container about-grid">
    <div class="about-content">
      <p class="eyebrow">{t.about.eyebrow}</p>
      <h2>{t.about.title}</h2>
      <p>{t.about.p1}</p>
      <p>{t.about.p2}</p>

      <div class="stats-grid">
        {#each t.about.stats as stat}
          <div class="stat-card">
            <h3>{stat.value}</h3>
            <p>{stat.label}</p>
          </div>
        {/each}
      </div>
    </div>

    <div class="about-visual">
      <img
        src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=1200&q=80"
        alt="Engineering team"
      />
      <div class="about-panel">
        <h3>{t.about.panelTitle}</h3>
        <p>{t.about.panelText}</p>
      </div>
    </div>
  </div>
</section>