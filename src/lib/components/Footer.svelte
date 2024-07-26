<script lang="ts">
  import { toggleMode } from 'mode-watcher'
  import Sun from 'lucide-svelte/icons/sun'
  import Moon from 'lucide-svelte/icons/moon'
  import { Button } from '$lib/components/ui/button'
</script>

<footer
  class="py-20 sm:py-32 bg-black border-t border-solid border-violet-950 flex flex-col gap-4 sm:gap-8 justify-center items-center"
>
  <div class="flex gap-20">
    <!-- <div
            class="flex items-center gap-4 sm:gap-6 text-2xl sm:text-3xl md:text-4xl mx-auto"
        >
            <a>
                <i class="fa-brands fa-linkedin-in" />
            </a>
            <a>
                <i class="fa-brands fa-github" />
            </a>
        </div>
        <p class="mx-auto text-sm opacity-70">or</p>
        <p class="">Hugh_jass@gmail.com</p> -->

    <p>
      <b class="pr-2">Documentation</b>
      <br /> Getting Started <br />
      API References <br /> Integrations <br /> Examples <br /> SDKs
    </p>
    <p>
      <b class="pr-3">Resources</b><br />
      Changelog<br />
      Pricing<br />
      Security<br />
      SOC 2<br />
      GDPR<br />
      Status<br />
      Brand<br />
    </p>
    <p>
      <b class="pr-3">Company</b><br />
      About<br />
      Blog<br />
      Careers<br />
      Contact<br />
      Customers<br />
      Philosophy<br />
    </p>
    <p>
      <b class="pr-3">Hand Book</b><br />
      Why we exist<br />
      How we work<br />
      Engineering<br />
      Design<br />
      Support<br />
      Marketing<br />
    </p>
    <p>
      <b class="pr-3">Legal</b><br />
      Acceptable Use<br />
      Cookie Policy<br />
      Privacy Policy<br />
      Terms of Service<br />
      Subprocessors<br />
      DPA<br />
    </p>
  </div>
</footer>

<Button on:click={toggleMode} variant="outline" size="icon">
  <Sun
    class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
  />
  <Moon
    class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
  />
  <span class="sr-only">Toggle theme</span>
</Button>
