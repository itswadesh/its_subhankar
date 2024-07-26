<script>
  import Footer from '$lib/components/Footer.svelte'
  import Header from '$lib/components/Header.svelte'
  import { ModeWatcher } from 'mode-watcher'
  import '../app.pcss'
  let y = 0
  let innerWidth = 0
  let innerHeight = 0

  function goTop() {
    document.body.scrollIntoView()
  }
</script>

<ModeWatcher />

<div
  class="container relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
>
  <div
    class={'fixed bottom-0 w-full duration-200 flex p-10 ' +
      (y > 0 ? '  pointer-events-auto' : ' pointer-events-none')}
  >
    <button
      on:click={goTop}
      class="ml-auto rounded-full bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer aspect-square grid place-items-center"
    >
      <i class="fa-solid fa-arrow-up" />
    </button>
  </div>
  <Header {y} {innerHeight} />
  <slot />
  <Footer />
</div>
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
