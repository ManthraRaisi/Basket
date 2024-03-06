<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: ["Personalized Recommendations:"],
      description:
        "Basket employs advanced algorithms to analyze your browsing and purchase history, providing tailored product recommendations suited to your preferences. Discover new items you'll love effortlessly, enhancing your shopping experience.",
      imgUrl: "assets/selection.jpg",
    },
    {
      featureList: ["One-Click Reordering:"],
      description:
        "Streamline your shopping routine with the convenience of one-click reordering. Easily repurchase your favorite items or essentials without navigating through multiple steps, saving you time and effort.",
      imgUrl: "assets/training.jpg",
    },
    {
      featureList: ["Virtual Try-On Technology"],
      description:
        "Explore our innovative virtual try-on feature, allowing you to visualize how products will look before purchasing. Whether trying on clothing, accessories, or even furniture, this immersive experience ensures confidence in your buying decisions, minimizing returns and enhancing satisfactio.",
      imgUrl: "assets/goal.jpg",
    },
  ];
</script>

<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Shop smart with y<span class="text-indigo-400">Basket</span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Features tailored for everyone.
      </h3>
    </div>

    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          enhancing your <span class="text-indigo-400 font-medium"
            >shopping</span
          >
          experience.
        {:else if index === 1}
          shopping routine with <span class="text-indigo-400 font-medium"
            >one-clicK</span
          > reordering
        {:else}
          innovative virtual <span class="text-indigo-400 font-medium">
            try-ont</span
          >
          feature
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
