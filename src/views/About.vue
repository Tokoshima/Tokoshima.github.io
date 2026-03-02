<script setup>
import { computed } from 'vue'
import { marked } from 'marked'
import { useRouter } from 'vue-router'
import rawMd from '../assets/about.md?raw'

const router = useRouter()
const rendered = computed(() => marked.parse(rawMd))
</script>

<template>
  <div class="page">

    <div class="top-bar">
      <button class="btn-back" @click="router.push('/')">← back</button>
      <span class="page-label">// about</span>
    </div>

    <div class="content-wrap">
      <div class="prose" v-html="rendered" />
    </div>

  </div>
</template>

<style scoped>
.page {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 100%;
}

/* ── top bar ─────────────────────────────────────────── */
.top-bar {
  background: #fff;
  padding: 1rem 2rem;
  border-left: 5px solid #444;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.page-label {
  font-size: 0.72rem;
  letter-spacing: 0.2em;
  color: #777;
  flex: 1;
  text-align: center;
}

.btn-back {
  background: none;
  border: none;
  font-family: "Courier New", Courier, monospace;
  font-size: 0.78rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  cursor: pointer;
  padding: 0.3rem 0.6rem;
  color: #444;
  border-bottom: 2px solid transparent;
  transition: border-color 0.15s, transform 0.15s;
}

.btn-back:hover {
  border-bottom-color: #444;
  transform: translateY(-1px);
}

/* ── content ─────────────────────────────────────────── */
.content-wrap {
  background: #fff;
  border-left: 5px solid #444;
  border-top: 4px solid #444;
  padding: 2.8rem 3.2rem;
  min-height: 340px;
}


/* ── rendered markdown ───────────────────────────────── */
.prose {
  font-family: "Courier New", Courier, monospace;
  font-size: 0.9rem;
  line-height: 2.2;
  color: #333;
  letter-spacing: 0.02em;
}

.prose :deep(h1) {
  font-size: 1.8rem;
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: -0.02em;
  margin: 0 0 1.4rem;
  color: #222;
}

.prose :deep(h2) {
  font-size: 1rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  margin: 2rem 0 0.8rem;
  color: #333;
  border-bottom: 2px solid #e0e0e0;
  padding-bottom: 0.3rem;
}

.prose :deep(p) {
  margin: 0 0 1rem;
}

.prose :deep(ul) {
  padding-left: 1.4rem;
  margin: 0 0 1rem;
}

.prose :deep(li) {
  margin-bottom: 0.3rem;
}

.prose :deep(a) {
  color: #333;
  text-decoration: underline;
  text-underline-offset: 3px;
}

.prose :deep(a:hover) {
  background-image: linear-gradient(
    168deg,
    #444 2.17%, #f0f0f0 2.17%, #f0f0f0 50%,
    #444 50%, #444 52.17%, #f0f0f0 52.17%, #f0f0f0 100%
  );
  background-size: 23px 5px;
  text-decoration: none;
}

.prose :deep(hr) {
  border: none;
  border-top: 2px solid #e0e0e0;
  margin: 1.5rem 0;
}

.prose :deep(strong) {
  font-weight: 700;
  color: #222;
}
</style>
