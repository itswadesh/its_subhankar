<script>
  import { Button } from '$lib/components/ui/button'

  export let y

  export let tabs = [
    { name: 'About ', link: '/about' },
    { name: 'Blog', link: '/blog' },
    { name: 'Customers ', link: '/customers' },
    { name: 'Resources ', link: '/resources ' },
    { name: 'Docs ', link: '/docs' },
    { name: 'Pricing ', link: '/pricing' },
    { name: 'Sign in ', link: '/sign-in' }
    // { name: "Contact", link: "" },
    // {name: '', link: ''},
  ]
</script>

<header
  class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid ' +
    (y > 0
      ? ' py-4 bg-background border-violet-950'
      : ' py-6 bg-background border-transparent')}
>
  <h1 class="font-medium">
    <a href="/" class="font-bold poppins">RESEND</a>
  </h1>
  <div class="sm:flex items-center gap-4 hidden">
    {#each tabs as tab, index}
      <a
        href={tab.link}
        class="duration-200 hover:text-violet-400"
        target={index === 2 ? '_blank' : ''}
      >
        <p>{tab.name}</p>
      </a>
    {/each}
    <!-- <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-violet-600 text-white"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Login</h4>
        </button> -->
    <Button class="px-5 py-2 group rounded-full">Get Started</Button>
  </div>
</header>
