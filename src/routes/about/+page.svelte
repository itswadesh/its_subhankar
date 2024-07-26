<script lang="ts">
  import { Slider } from '$lib/components/ui/slider'
  let emailCount = [33]
</script>

{emailCount}

<Slider bind:value={emailCount} max={100} step={1} />

<div class="flex flex-col gap-4 text-center justify-center items-center">
  <h6 class="text-large sm:text-xl md:text-2xl">Our story</h6>
  <div class="text-left max-w-md gap-4 grid grid-cols-1">
    <p>
      Resend started with an open source project in 2022. We were frustrated by
      how difficult it was to build modern email templates that worked well
      across all email clients.
    </p>
    <p>
      As we started to dig deeper, it became clear that this was just the tip of
      the iceberg. We realized that sending emails that reach the inbox (not the
      spam folder) was the biggest pain point, so we started to explore
      something new.
    </p>
    <p>
      In 2023, we launched an entire email sending platform and joined Y
      Combinator's winter batch. We're creating something special here, and
      we're excited to build it with you.
    </p>
  </div>
</div>
