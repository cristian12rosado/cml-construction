<script lang="ts">
  import { language } from '$lib/stores/language';
  import { content } from '$lib/data/content';

  $: t = content[$language ?? 'en'] ?? content.en;
</script>

<section id="contact" class="section contact-section">
  <div class="container contact-grid">
    <div class="contact-info">
      <p class="eyebrow">{t.contact.eyebrow}</p>
      <h2>{t.contact.title}</h2>
      <p>{t.contact.description}</p>

      <div class="info-list">
        <div>
          <span>{t.contact.addressLabel}</span>
          <p>{t.contact.address}</p>
        </div>
        <div>
          <span>{t.contact.phoneLabel}</span>
          <p>{t.contact.phone}</p>
        </div>
        <div>
          <span>{t.contact.emailLabel}</span>
          <p>{t.contact.email}</p>
        </div>
      </div>
    </div>

    <form class="contact-form">
      <div class="form-group">
        <label for="name">{t.contact.form.name}</label>
        <input id="name" type="text" placeholder={t.contact.form.namePlaceholder} />
      </div>

      <div class="form-group">
        <label for="email">{t.contact.form.email}</label>
        <input id="email" type="email" placeholder={t.contact.form.emailPlaceholder} />
      </div>

      <div class="form-group">
        <label for="company">{t.contact.form.company}</label>
        <input id="company" type="text" placeholder={t.contact.form.companyPlaceholder} />
      </div>

      <div class="form-group">
        <label for="message">{t.contact.form.message}</label>
        <textarea id="message" rows="5" placeholder={t.contact.form.messagePlaceholder}></textarea>
      </div>

      <button type="submit" class="btn btn-primary full">{t.contact.form.submit}</button>
    </form>
  </div>
</section>