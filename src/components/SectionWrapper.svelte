<script>
  /**
   * @type {any}
   */
  export let id = null;
</script>

<section {id} class={"min-h-screen flex flex-col"}>
  <div class="flex flex-col flex-1 max-w-[1400px] mx-auto w-full p-4">
    <slot />
  </div>
</section>
