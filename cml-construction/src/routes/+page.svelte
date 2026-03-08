<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import Services from '$lib/components/Services.svelte';
  import Projects from '$lib/components/Projects.svelte';
  import About from '$lib/components/About.svelte';
  import Contact from '$lib/components/Contact.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>Civil Engineering</title>
  <meta
    name="description"
    content="Modern bilingual civil engineering website in English and Spanish."
  />
</svelte:head>

<div class="page">
  <Header />
  <Hero />
  <Services />
  <Projects />
  <About />
  <Contact />
  <Footer />
</div>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    margin: 0;
    font-family:
      Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: #050505;
    color: #ffffff;
  }

  :global(*) {
    box-sizing: border-box;
  }

  :global(.page) {
    background:
      radial-gradient(circle at top, rgba(255, 106, 0, 0.08), transparent 30%),
      linear-gradient(to bottom, #060606, #0b0b0b 35%, #050505 100%);
    min-height: 100vh;
  }

  :global(.container) {
    width: min(1180px, calc(100% - 2rem));
    margin: 0 auto;
  }

  :global(.site-header) {
    position: sticky;
    top: 0;
    z-index: 50;
    background: rgba(0, 0, 0, 0.82);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  }

  :global(.nav) {
    display: flex;
    align-items: center;
    justify-content: space-between;
    min-height: 82px;
    gap: 1rem;
  }

  :global(.brand) {
    display: flex;
    align-items: center;
    gap: 0.85rem;
  }

  :global(.brand-mark) {
    width: 44px;
    height: 44px;
    border: 2px solid #ff6a00;
    color: #ff6a00;
    border-radius: 12px;
    display: grid;
    place-items: center;
    font-size: 1.2rem;
    font-weight: 800;
  }

  :global(.brand-text) {
    display: flex;
    flex-direction: column;
    line-height: 0.95;
    font-weight: 800;
    letter-spacing: 0.04em;
  }

  :global(.desktop-nav) {
    display: flex;
    gap: 2rem;
  }

  :global(.desktop-nav a),
  :global(.site-footer a) {
    color: #ffffff;
    text-decoration: none;
  }

  :global(.desktop-nav a:hover),
  :global(.site-footer a:hover) {
    color: #ff6a00;
  }

  :global(.lang-switch) {
    display: flex;
    gap: 0.5rem;
  }

  :global(.lang-switch button) {
    background: transparent;
    color: white;
    border: 1px solid rgba(255,255,255,0.2);
    padding: 0.5rem 0.75rem;
    border-radius: 10px;
    cursor: pointer;
  }

  :global(.lang-switch button.active) {
    background: #ff6a00;
    border-color: #ff6a00;
  }

  :global(.hero) {
    position: relative;
    min-height: 92vh;
    display: flex;
    align-items: center;
    overflow: hidden;
  }

  :global(.hero-image) {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: grayscale(35%) brightness(0.35);
  }

  :global(.hero-overlay) {
    position: absolute;
    inset: 0;
    background:
      linear-gradient(90deg, rgba(0, 0, 0, 0.88) 0%, rgba(0, 0, 0, 0.68) 40%, rgba(0, 0, 0, 0.5) 100%),
      linear-gradient(to top, rgba(0, 0, 0, 0.85), transparent 40%);
  }

  :global(.hero-content) {
    position: relative;
    z-index: 1;
    padding: 5rem 0;
    max-width: 760px;
  }

  :global(.eyebrow) {
    color: #ff6a00;
    text-transform: uppercase;
    letter-spacing: 0.16em;
    font-size: 0.78rem;
    font-weight: 700;
    margin-bottom: 1rem;
  }

  :global(.hero h1) {
    font-size: clamp(3.5rem, 8vw, 6.5rem);
    line-height: 0.92;
    margin: 0 0 1.25rem 0;
    letter-spacing: -0.04em;
  }

  :global(.hero-copy) {
    max-width: 620px;
    color: rgba(255, 255, 255, 0.82);
    font-size: 1.08rem;
    line-height: 1.75;
    margin-bottom: 2rem;
  }

  :global(.hero-actions) {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  :global(.btn) {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    border-radius: 12px;
    padding: 0.95rem 1.4rem;
    font-weight: 800;
    cursor: pointer;
  }

  :global(.btn-primary) {
    background: linear-gradient(135deg, #ff7b1a, #ff5a00);
    color: white;
    border: none;
  }

  :global(.btn-outline) {
    background: rgba(255, 255, 255, 0.02);
    color: white;
    border: 1px solid rgba(255, 255, 255, 0.18);
  }

  :global(.section) {
    padding: 6rem 0;
  }

  :global(.section-dark) {
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0.01), rgba(255, 255, 255, 0.02));
  }

  :global(.section-heading) {
    max-width: 760px;
    margin-bottom: 2.5rem;
  }

  :global(.section-heading h2) {
    font-size: clamp(2rem, 4vw, 3rem);
    margin: 0 0 1rem 0;
  }

  :global(.section-heading p:last-child) {
    color: rgba(255, 255, 255, 0.72);
    line-height: 1.8;
    margin: 0;
  }

  :global(.services-grid) {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1.25rem;
  }

  :global(.service-card) {
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.03), rgba(255, 255, 255, 0.015));
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 20px;
    padding: 1.6rem;
  }

  :global(.service-icon) {
    width: 56px;
    height: 56px;
    border-radius: 14px;
    display: grid;
    place-items: center;
    margin-bottom: 1rem;
    color: #ff6a00;
    background: rgba(255, 106, 0, 0.08);
    border: 1px solid rgba(255, 106, 0, 0.2);
    font-size: 1.3rem;
  }

  :global(.project-filters) {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
    margin-bottom: 1.75rem;
  }

  :global(.project-filters button) {
    background: transparent;
    color: rgba(255, 255, 255, 0.72);
    border: 1px solid rgba(255, 255, 255, 0.12);
    padding: 0.7rem 1rem;
    border-radius: 999px;
  }

  :global(.project-filters button.active) {
    color: white;
    border-color: rgba(255, 106, 0, 0.45);
    background: rgba(255, 106, 0, 0.12);
  }

  :global(.projects-grid) {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
  }

  :global(.project-card) {
    position: relative;
    border-radius: 22px;
    overflow: hidden;
    min-height: 360px;
  }

  :global(.project-card img) {
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: brightness(0.72);
  }

  :global(.project-overlay) {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 1.4rem;
    background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent 55%);
  }

  :global(.project-category) {
    display: inline-flex;
    width: fit-content;
    padding: 0.35rem 0.65rem;
    border-radius: 999px;
    background: rgba(255, 106, 0, 0.16);
    color: #ff8c3a;
    font-size: 0.78rem;
    font-weight: 700;
    margin-bottom: 0.8rem;
  }

  :global(.project-link) {
    width: fit-content;
    color: white;
    text-decoration: none;
    padding: 0.75rem 1rem;
    border-radius: 12px;
    background: linear-gradient(135deg, #ff7b1a, #ff5a00);
    font-weight: 700;
  }

  :global(.about-grid),
  :global(.contact-grid) {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    align-items: center;
  }

  :global(.stats-grid) {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-top: 2rem;
  }

  :global(.stat-card) {
    padding: 1.3rem;
    border-radius: 18px;
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.07);
  }

  :global(.stat-card h3) {
    margin: 0 0 0.4rem 0;
    font-size: 2rem;
    color: #ff6a00;
  }

  :global(.about-visual) {
    position: relative;
  }

  :global(.about-visual img) {
    width: 100%;
    min-height: 560px;
    object-fit: cover;
    border-radius: 24px;
    display: block;
    filter: brightness(0.72);
  }

  :global(.about-panel) {
    position: absolute;
    left: 1rem;
    right: 1rem;
    bottom: 1rem;
    padding: 1.4rem;
    border-radius: 18px;
    background: rgba(0, 0, 0, 0.78);
  }

  :global(.info-list) {
    display: grid;
    gap: 1.2rem;
    margin-top: 2rem;
  }

  :global(.info-list span) {
    color: #ff6a00;
    font-size: 0.85rem;
    font-weight: 700;
    text-transform: uppercase;
  }

  :global(.contact-form) {
    padding: 1.6rem;
    border-radius: 24px;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.03), rgba(255, 255, 255, 0.015));
    border: 1px solid rgba(255, 255, 255, 0.08);
  }

  :global(.form-group) {
    display: grid;
    gap: 0.55rem;
    margin-bottom: 1rem;
  }

  :global(.form-group input),
  :global(.form-group textarea) {
    width: 100%;
    border: 1px solid rgba(255, 255, 255, 0.12);
    background: rgba(255, 255, 255, 0.03);
    color: white;
    border-radius: 14px;
    padding: 0.95rem 1rem;
    font: inherit;
  }

  :global(.full) {
    width: 100%;
  }

  :global(.site-footer) {
    border-top: 1px solid rgba(255, 255, 255, 0.08);
    background: #030303;
    padding-top: 3rem;
  }

  :global(.footer-grid) {
    display: grid;
    grid-template-columns: 1.4fr 1fr 1fr 1fr;
    gap: 2rem;
  }

  :global(.footer-copy) {
    color: rgba(255, 255, 255, 0.64);
    max-width: 360px;
    line-height: 1.75;
  }

  :global(.site-footer ul) {
    list-style: none;
    padding: 0;
    margin: 0;
    display: grid;
    gap: 0.75rem;
    color: rgba(255, 255, 255, 0.7);
  }

  :global(.footer-bottom) {
    padding: 1.5rem 0 2rem;
    margin-top: 2.5rem;
    border-top: 1px solid rgba(255, 255, 255, 0.06);
  }

  :global(.footer-bottom p) {
    margin: 0;
    color: rgba(255, 255, 255, 0.48);
  }

  @media (max-width: 1100px) {
    :global(.services-grid),
    :global(.projects-grid),
    :global(.stats-grid) {
      grid-template-columns: repeat(2, 1fr);
    }

    :global(.about-grid),
    :global(.contact-grid),
    :global(.footer-grid) {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 760px) {
    :global(.desktop-nav) {
      display: none;
    }

    :global(.services-grid),
    :global(.projects-grid),
    :global(.stats-grid) {
      grid-template-columns: 1fr;
    }

    :global(.section) {
      padding: 4.5rem 0;
    }

    :global(.hero h1) {
      font-size: 3.2rem;
    }
  }
</style>