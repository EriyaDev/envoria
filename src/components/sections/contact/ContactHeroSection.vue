<script setup></script>

<template>
  <section class="min-h-[80vh] lg:min-h-screen bg-secondary-color">
    <div
      class="grid grid-cols-5 lg:grid-cols-10 max-w-[90%] mx-auto lg:max-w-full gap-10 px-3 md:px-0"
    >
      <!-- LEFT: Text -->
      <div
        class="flex flex-col justify-center text-left py-16 h-[80vh] lg:h-screen w-full lg:max-w-[70%] lg:mx-auto col-span-5 lg:col-span-10 xl:col-span-5"
      >
        <h1 class="text-display font-semibold mb-6">Get in touch with us</h1>
        <p
          class="text-body text-text-primary-color/75 leading-relaxed mb-8 md:max-w-[70%] lg:max-w-[90%]"
        >
          Every clean environment starts with a conversation. Whether you're managing industrial
          waste or scaling your recycling operations, Envoria is here to help.
        </p>
        <div class="flex items-center gap-2">
          <!-- Instagram -->
          <a
            href="#"
            aria-label="Instagram"
            class="w-9 h-9 bg-accent-color hover:brightness-95 rounded-full flex items-center justify-center transition-colors"
          >
            <svg
              width="16"
              height="16"
              viewBox="0 0 24 24"
              fill="none"
              stroke="#121212"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <rect x="2" y="2" width="20" height="20" rx="5" ry="5" />
              <circle cx="12" cy="12" r="4" />
              <circle cx="17.5" cy="6.5" r="1" fill="#121212" stroke="none" />
            </svg>
          </a>

          <!-- Facebook -->
          <a
            href="#"
            aria-label="Facebook"
            class="w-9 h-9 bg-accent-color hover:brightness-95 rounded-full flex items-center justify-center transition-colors"
          >
            <svg width="16" height="16" viewBox="0 0 24 24" fill="#121212">
              <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z" />
            </svg>
          </a>

          <!-- X (Twitter) -->
          <a
            href="#"
            aria-label="X"
            class="w-9 h-9 bg-accent-color hover:brightness-95 rounded-full flex items-center justify-center transition-colors"
          >
            <svg width="15" height="15" viewBox="0 0 24 24" fill="#121212">
              <path
                d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"
              />
            </svg>
          </a>

          <!-- LinkedIn -->
          <a
            href="#"
            aria-label="LinkedIn"
            class="w-9 h-9 bg-[#4ade00] hover:bg-[#39c400] rounded-full flex items-center justify-center transition-colors"
          >
            <svg width="15" height="15" viewBox="0 0 24 24" fill="#121212">
              <path
                d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
              />
              <rect x="2" y="9" width="4" height="12" />
              <circle cx="4" cy="4" r="2" />
            </svg>
          </a>
        </div>
      </div>

      <!-- RIGHT: Image -->
      <div
        class="lg:h-screen hidden xl:flex items-center justify-center w-full col-span-5 lg:col-span-3 xl:col-span-5"
      >
        <img
          class="w-full h-full object-cover"
          src="../../../assets/images/contact-hero/contect-hero.webp"
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.marquee-wrapper {
  display: flex;
  gap: 20px;
  height: 100vh;
}

/* ── Each column ── */
.marquee-col {
  overflow: hidden; /* clip content that scrolls out of view */
  position: relative;
}

/* Fade masks top & bottom for a polished edge */
.marquee-col::before,
.marquee-col::after {
  content: '';
  position: absolute;
  left: 0;
  right: 0;
  height: 120px;
  z-index: 2;
  pointer-events: none;
}
.marquee-col::before {
  top: 0;
  background: linear-gradient(to bottom, #0a0a0a, transparent);
}
.marquee-col::after {
  bottom: 0;
  background: linear-gradient(to top, #0a0a0a, transparent);
}

/* ── The inner track that GSAP moves ── */
.marquee-track {
  display: flex;
  flex-direction: column;
  gap: 16px;
  will-change: transform; /* hint browser for GPU compositing */
}

/* ── Individual card ── */
.marquee-card {
  height: 350px;
  border-radius: 16px;
  overflow: hidden;
  flex-shrink: 0;
  position: relative;
}

.marquee-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s ease;
}

.marquee-card:hover img {
  transform: scale(1.06);
}

/* subtle overlay label */
.marquee-card .label {
  position: absolute;
  bottom: 12px;
  left: 12px;
  background: rgba(255, 255, 255, 0.12);
  backdrop-filter: blur(8px);
  color: #fff;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 5px 10px;
  border-radius: 100px;
}
</style>
