<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content, projects } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<section id="projects" class="section">
  <div class="container">
    <div class="section-heading">
      <p class="eyebrow">{t.projects.eyebrow}</p>
      <h2>{t.projects.title}</h2>
      <p>{t.projects.description}</p>
    </div>

    <div class="project-filters">
      {#each t.projects.filters as filter, i}
        <button class:active={i === 0}>{filter}</button>
      {/each}
    </div>

    <div class="projects-grid">
      {#each projects as project}
        <article class="project-card">
          <img src={project.image} alt={project.title[$language ?? 'en'] ?? project.title.en} />
          <div class="project-overlay">
            <span class="project-category">
              {project.category[$language ?? 'en'] ?? project.category.en}
            </span>
            <h3>{project.title[$language ?? 'en'] ?? project.title.en}</h3>
          </div>
        </article>
      {/each}
    </div>
  </div>
</section>