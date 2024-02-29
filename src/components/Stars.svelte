<div class="flex items-center justify-center gap-2 text-base">
  <p>3</p>
  {#each [0, 1, 2, 3, 4] as index}
    <div class="grid place-items-center relative">
      <i class="fa-solid fa-star opacity-0"></i>
      <div
        class={"absolute top-0 left-0 grid place-items-center " +
          (index === 3 ? "w-[0%] overflow-hidden" : " ")}
      >
        <i class="fa-solid fa-star text-amber-400"></i>
      </div>
    </div>
  {/each}
  <p>500+</p>
</div>
