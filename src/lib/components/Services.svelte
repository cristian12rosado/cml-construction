<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<section id="services" class="section section-dark">
  <div class="container">
    <div class="section-heading">
      <p class="eyebrow">{t.services.eyebrow}</p>
      <h2>{t.services.title}</h2>
      <p>{t.services.description}</p>
    </div>

    <div class="services-grid">
      {#each t.services.items as service}
        <article class="service-card">
          <div class="service-icon">⌁</div>
          <h3>{service.title}</h3>
          <p>{service.description}</p>
        </article>
      {/each}
    </div>
  </div>
</section>