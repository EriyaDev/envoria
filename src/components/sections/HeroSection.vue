<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import { ref, onMounted, onUnmounted } from 'vue'
import Typed from 'typed.js'
import gsap from 'gsap'

const typedEl = ref(null)
let typed = null

onMounted(() => {
  typed = new Typed(typedEl.value, {
    strings: ['cleaner world', 'better environment', 'healthier earth'],
    typeSpeed: 60,
    backSpeed: 40,
    loop: true,
    // showCursor: false,
  })
})

// onMounted(() => {
//   const leftCol = document.querySelector('.hero-col-left')
//   const rightCol = document.querySelector('.hero-col-right')

//   const totalHeight = leftCol.scrollHeight / 2 // separuh = 1 set asli

//   // LEFT — scroll ke atas
//   gsap.to(leftCol, {
//     y: -totalHeight,
//     duration: 8,
//     ease: 'none',
//     repeat: -1,
//     modifiers: {
//       y: gsap.utils.unitize((y) => parseFloat(y) % totalHeight),
//     },
//   })

//   // RIGHT — scroll ke bawah
//   gsap.fromTo(
//     rightCol,
//     { y: -totalHeight },
//     {
//       y: 0,
//       duration: 8,
//       ease: 'none',
//       repeat: -1,
//       modifiers: {
//         y: gsap.utils.unitize((y) => {
//           const val = parseFloat(y) % totalHeight
//           return val > 0 ? val - totalHeight : val
//         }),
//       },
//     },
//   )
// })

onUnmounted(() => {
  typed.destroy()
})

onMounted(() => {
  /*
   * INFINITE VERTICAL MARQUEE TECHNIQUE
   * ─────────────────────────────────────
   * 1. Duplicate the set of cards once → track = [A, B, C, A', B', C']
   * 2. The track height = 3 cards + gaps (one set).
   * 3. GSAP animates translateY from 0 → -oneSetHeight  (upward)
   *    or from -oneSetHeight → 0  (downward).
   * 4. repeat: -1 + ease: "none" = perfect seamless loop with zero jump.
   */

  function setupMarquee(trackId, direction) {
    const track = document.getElementById(trackId)

    // ── Step 1: Clone the original cards and append to track ──
    // This gives us a double-length strip so the loop feels continuous.
    const origCards = Array.from(track.children)
    origCards.forEach((card) => {
      const clone = card.cloneNode(true)
      track.appendChild(clone)
    })

    // ── Step 2: Measure ONE full set height (cards + gaps) ──
    // card height (280) × 3 cards + gap (16) × 3 gaps
    const cardH = 350
    const gap = 16
    const setCount = origCards.length // 3
    const oneSetH = setCount * cardH + setCount * gap // 888px

    // ── Step 3: Set start position for downward column ──
    // Upward   → starts at y:0,         ends at y:-oneSetH
    // Downward → starts at y:-oneSetH,  ends at y:0
    // Both reach the clone boundary and restart invisibly.
    if (direction === 'down') {
      gsap.set(track, { y: -oneSetH }) // start offset so it scrolls into view
    }

    // ── Step 4: Animate with GSAP ──
    // ease:"none" is critical — any ease creates speed variation at loop seam.
    // repeat:-1 loops infinitely; the y jump is imperceptible because
    // position 0 and -oneSetH show identical pixel content.
    gsap.to(track, {
      y: direction === 'up' ? -oneSetH : 0, // destination
      duration: 18, // seconds for one full cycle (adjust speed here)
      ease: 'none', // constant velocity = seamless
      repeat: -1, // loop forever

      // For upward: reset from -oneSetH back to 0 (invisible jump)
      // For downward: reset from 0 back to -oneSetH (invisible jump)
      modifiers: {
        y: gsap.utils.unitize((y) => {
          if (direction === 'up') {
            // wrap: once we pass -oneSetH, jump back to 0
            return parseFloat(y) % oneSetH
          } else {
            // wrap: once we reach 0, jump back to -oneSetH
            let val = parseFloat(y) % oneSetH
            if (val > 0) val -= oneSetH
            return val
          }
        }),
      },
    })
  }

  // Pause on hover — feels premium and lets users inspect cards
  function addHoverPause(colId, trackId) {
    const col = document.getElementById(colId)
    const track = document.getElementById(trackId)

    col.addEventListener('mouseenter', () => {
      gsap.to(gsap.getTweensOf(track), { timeScale: 0, duration: 0.5, ease: 'power2.out' })
    })
    col.addEventListener('mouseleave', () => {
      gsap.to(gsap.getTweensOf(track), { timeScale: 1, duration: 0.8, ease: 'power2.inOut' })
    })
  }

  // ── Initialise both columns ──
  setupMarquee('track-left', 'up')
  setupMarquee('track-right', 'down')

  addHoverPause('col-left', 'track-left')
  addHoverPause('col-right', 'track-right')
})
</script>

<template>
  <section class="min-h-[80vh] lg:min-h-screen bg-secondary-color">
    <div class="grid grid-cols-5 lg:grid-cols-10 section-container gap-10 px-3 md:px-0">
      <!-- LEFT: Text -->
      <div
        class="flex flex-col justify-center text-left py-16 h-[80vh] lg:h-screen w-full col-span-5 lg:col-span-10 xl:col-span-5"
      >
        <h1 class="text-display font-semibold mb-6">
          Innovation rooted in nature for a <span ref="typedEl"></span>
        </h1>
        <p class="text-body text-gray-500 leading-relaxed mb-8 md:max-w-[70%]">
          Join a community of eco-enthusiasts taking meaningful actions to protect nature and create
          a greener future.
        </p>
        <div class="flex flex-col lg:flex-row lg:items-center gap-3 md:gap-5">
          <button
            class="bg-black w-fit flex items-center gap-1 text-white font-family-inter text-base py-3 px-6 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer"
          >
            <img src="../../assets/icons/home/leaf.svg" alt="" />
            <p class="text-body font-medium">Join Action</p>
          </button>
          <ButtonPrimary to="/about">
            <img src="../../assets/icons/home/heart.svg" alt="" />
            <p class="text-body">Donate Now</p></ButtonPrimary
          >
        </div>
      </div>

      <!-- RIGHT: Image -->
      <div
        class="lg:h-screen hidden xl:flex items-center justify-center w-full col-span-5 lg:col-span-3 xl:col-span-5"
      >
        <div class="marquee-wrapper">
          <!-- ── LEFT column — scrolls UPWARD ── -->
          <div class="marquee-col relative overflow-hidden lg:w-[215px]" id="col-left">
            <div class="marquee-track" id="track-left">
              <!-- original set -->
              <div class="marquee-card">
                <img src="../../assets/images/hero/lt.webp" alt="hero-1" />
              </div>
              <div class="marquee-card">
                <img src="../../assets/images/hero/lm.webp" alt="hero-2" />
              </div>
              <div class="marquee-card">
                <img src="../../assets/images/hero/lb.webp" alt="hero-3" />
              </div>
              <!-- cloned set — appended by JS for seamless loop -->
            </div>
          </div>

          <!-- ── RIGHT column — scrolls DOWNWARD ── -->
          <div class="marquee-col relative overflow-hidden lg:w-[215px]" id="col-right">
            <div class="marquee-track" id="track-right">
              <!-- original set -->
              <div class="marquee-card">
                <img src="../../assets/images/hero/rt.webp" alt="hero-1" />
              </div>
              <div class="marquee-card">
                <img src="../../assets/images/hero/rm.webp" alt="hero-2" />
              </div>
              <div class="marquee-card">
                <img src="../../assets/images/hero/rb.webp" alt="hero-3" />
              </div>
              <!-- cloned set — appended by JS for seamless loop -->
            </div>
          </div>
        </div>
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
