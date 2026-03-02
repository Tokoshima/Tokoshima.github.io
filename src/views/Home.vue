<template>
  <div class="site">

    <header class="block name-block">
      <span class="eyebrow"></span>
      <h1 class="name">Louw<br>Pretorius</h1>
    </header>

    <div class="block bio-block">
      <p class="bio">
        jack of all trades, master of a few.<br>
        here you will find a summary of what i am,<br>
        what i can do, and why i might be worth your time.
      </p>
    </div>

    <nav class="nav-grid">
      <router-link class="nav-item" to="/about">About</router-link>
      <a class="nav-item" href="https://github.com/Tokoshima" target="_blank">Github</a>
      <router-link class="nav-item" to="/resume">Resume</router-link>
      <a class="nav-item" href="#">Misc</a>
    </nav>

  </div>
</template>

<style scoped>
/* ── layout ─────────────────────────────────────────── */
.site {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

/* ── shared block ────────────────────────────────────── */
.block {
  background: #fff;
  padding: 2.8rem 3.2rem;
  border-left: 5px solid #444;
}

/* ── name / header ───────────────────────────────────── */
.name-block {
  padding-bottom: 2rem;
  position: relative;
}

.eyebrow {
  display: block;
  font-size: 0.72rem;
  letter-spacing: 0.2em;
  color: #777;
  margin-bottom: 1rem;
  text-transform: lowercase;
}

.name {
  font-size: clamp(2.6rem, 9vw, 4.5rem);
  font-weight: 900;
  line-height: 0.95;
  letter-spacing: -0.03em;
  font-family: "Courier New", Courier, monospace;
  text-transform: uppercase;
}

/* ── bio ─────────────────────────────────────────────── */
.bio-block {
  border-top: 4px solid #444;
}

.bio {
  font-size: 0.9rem;
  line-height: 2.4;
  letter-spacing: 0.04em;
  color: #333;
}

/* ── navigation ──────────────────────────────────────── */
.nav-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.nav-item {
  background: #fff;
  padding: 1.4rem 0.5rem;
  text-align: center;
  font-size: 0.78rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  font-weight: 700;
  font-family: "Courier New", Courier, monospace;
  border-top: 4px solid #444;
  border-left: 5px solid #444;
  transition: background-image 0.1s, color 0.1s, transform 0.15s;
  color: #333;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-item:hover {
  background-image: linear-gradient(
    168deg,
    #444 2.17%, #f0f0f0 2.17%, #f0f0f0 50%,
    #444 50%, #444 52.17%, #f0f0f0 52.17%, #f0f0f0 100%
  );
  background-size: 23px 5px;
  background-color: #fff;
  color: #333;
  transform: translateY(-3px);
}

/* ── responsive ──────────────────────────────────────── */
@media (max-width: 480px) {
  .block {
    padding: 1.5rem;
  }
  .nav-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
