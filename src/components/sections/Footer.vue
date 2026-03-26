<script setup></script>

<template>
  <footer class="w-full bg-card-color rounded-2xl overflow-hidden">
    <div class="section-container mx-auto pt-12 pb-8 grid grid-cols-1 lg:grid-cols-12 gap-12">
      <!-- LEFT: Brand + Newsletter (5 of 12 cols) -->
      <div class="lg:col-span-5 flex flex-col gap-8">
        <!-- Logo -->
        <img class="h-5 w-fit" src="../../assets/images/logo-footer.svg" alt="" />

        <!-- Newsletter -->
        <div class="flex flex-col gap-3">
          <p class="text-gray-900 font-semibold text-sm 2xl:text-base">
            Subscribe to our newsletter.
          </p>
          <!-- Input + Button row — Flexbox -->
          <div class="flex items-center gap-3">
            <input
              type="email"
              placeholder="Type your email"
              class="flex-1 min-w-0 bg-transparent border border-dashed border-gray-400 rounded-full px-4 py-2.5 text-sm 2xl:text-base text-gray-700 placeholder-gray-400 outline-none focus:border-gray-600 transition-colors"
            />
            <button
              class="bg-accent-color hover:brightness-95 text-gray-900 font-semibold text-sm 2xl:text-base px-5 py-2.5 rounded-full whitespace-nowrap transition-colors"
            >
              Subscribe
            </button>
          </div>
        </div>
      </div>

      <!-- RIGHT: 3-column link groups (7 of 12 cols) -->
      <!-- Inner grid: 3 equal columns -->
      <div
        class="lg:col-span-4 lg:col-start-8 grid grid-cols-3 gap-6 lg:justify-items-start lg:pl-8"
      >
        <!-- Pages -->
        <div class="flex flex-col gap-3">
          <h4 class="text-gray-900 font-semibold text-base">Pages</h4>
          <nav class="flex flex-col gap-2">
            <a
              href="#"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >Home</a
            >
            <a
              href="#"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >About us</a
            >
            <a
              href="#"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >Program</a
            >
            <a
              href="#"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >Blog</a
            >
            <a
              href="#"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >Contact us</a
            >
          </nav>
        </div>

        <!-- Contact -->
        <div class="flex flex-col gap-3">
          <h4 class="text-gray-900 font-semibold text-base">Contact</h4>
          <div class="flex flex-col gap-2">
            <a
              href="tel:+1234567890"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >+123-456-7890</a
            >
            <a
              href="tel:+9876543210"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >+987-654-3210</a
            >
          </div>
        </div>

        <!-- Mail -->
        <div class="flex flex-col gap-3">
          <h4 class="text-gray-900 font-semibold text-base">Mail</h4>
          <div class="flex flex-col gap-2">
            <a
              href="mailto:hello@example.com"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >hello@example.com</a
            >
            <a
              href="mailto:hello@envoria.com"
              class="text-gray-600 hover:text-gray-900 text-sm 2xl:text-base transition-colors"
              >hello@envoria.com</a
            >
          </div>
        </div>
      </div>
    </div>
    <div class="section-container mx-auto">
      <hr class="border-dashed border-gray-400/60" />
    </div>
    <div
      class="section-container mx-auto py-5 flex flex-col sm:flex-row items-center justify-between gap-4"
    >
      <!-- Copyright -->
      <p class="text-gray-700 text-sm 2xl:text-base">
        © 2017 - 2026
        <a href="#" class="text-text-primary-color/55 hover:underline font-medium">Envoria™</a>
        All rights reserved.
      </p>

      <!-- Social Icons — Flexbox row -->
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
  </footer>
</template>
