<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<footer class="site-footer">
  <div class="container footer-grid">
    <div>
      <div class="brand footer-brand">
        <div class="brand-mark">▦</div>
        <div class="brand-text">
          <span>CIVIL</span>
          <span>ENGINEERING</span>
        </div>
      </div>
      <p class="footer-copy">{t.footer.description}</p>
    </div>

    <div>
      <h4>{t.footer.quickLinks}</h4>
      <ul>
        <li><a href="#home">{t.nav.home}</a></li>
        <li><a href="#services">{t.nav.services}</a></li>
        <li><a href="#projects">{t.nav.projects}</a></li>
        <li><a href="#contact">{t.nav.contact}</a></li>
      </ul>
    </div>

    <div>
      <h4>{t.footer.services}</h4>
      <ul>
        {#each t.services.items as service}
          <li>{service.title}</li>
        {/each}
      </ul>
    </div>

    <div>
      <h4>{t.footer.contact}</h4>
      <ul>
        <li>{t.contact.address}</li>
        <li>{t.contact.phone}</li>
        <li>{t.contact.email}</li>
      </ul>
    </div>
  </div>

  <div class="container footer-bottom">
    <p>{t.footer.copyright}</p>
  </div>
</footer>