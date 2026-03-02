<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
</script>

<template>
  <div class="page">

    <div class="top-bar">
      <button class="btn-back" @click="router.push('/')">← back</button>
      <span class="page-label">// resume</span>
    </div>

    <div class="modal-wrap">
      <iframe src="/resume1.pdf#zoom=100" class="pdf-frame" />
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

/* ── pdf modal ───────────────────────────────────────── */
.modal-wrap {
  background: #fff;
  border-left: 5px solid #444;
  border-top: 4px solid #444;
  padding: 1.5rem;
  display: flex;
  justify-content: center;
}

.pdf-frame {
  width: 100%;
  max-width: 860px;
  height: 78vh;
  border: 1px solid #e0e0e0;
  display: block;
}
</style>
