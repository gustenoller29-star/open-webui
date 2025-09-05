<script>
  export let show = false;
  export let aiDiId = '';
  export let onClose = () => {};
</script>

{#if show}
  <div class="lunarno-modal-overlay">
    <div class="lunarno-modal">
      <div class="lunarno-modal-icon">
        <!-- Success icon SVG -->
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="24" cy="24" r="24" fill="#6EE7B7"/>
          <path d="M16 24L22 30L32 20" stroke="#065F46" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <h2 class="lunarno-modal-title">Connected to AiDi</h2>
      <p class="lunarno-modal-subtitle">ID: <span class="lunarno-modal-id">{aiDiId}</span></p>
      <button class="lunarno-modal-close" on:click={onClose}>Close</button>
    </div>
  </div>
{/if}

<style>
.lunarno-modal-overlay {
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0,0,0,0.4);
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
}
.lunarno-modal {
  background: #fff;
  border-radius: 1rem;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
  padding: 2rem 2.5rem;
  text-align: center;
  min-width: 320px;
}
.lunarno-modal-icon {
  margin-bottom: 1rem;
}
.lunarno-modal-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: #065F46;
  margin-bottom: 0.5rem;
}
.lunarno-modal-subtitle {
  font-size: 1rem;
  color: #374151;
  margin-bottom: 1.5rem;
}
.lunarno-modal-id {
  font-weight: 600;
  color: #10B981;
}
.lunarno-modal-close {
  background: #10B981;
  color: #fff;
  border: none;
  border-radius: 0.5rem;
  padding: 0.5rem 1.5rem;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.2s;
}
.lunarno-modal-close:hover {
  background: #065F46;
}
</style>
