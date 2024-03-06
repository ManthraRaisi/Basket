<script>
  import ReviewCard from "./ReviewCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let lim = true;
  let ReviewsList = [
    {
      name: " Sarah123",
      review:
        "Absolutely love Basket! The personalized recommendations feature always suggests items that match my style perfectly. Makes shopping so much easier! Also, the one-click reordering saves me time when restocking my essentials, and the virtual try-on feature helps me visualize how items will look before purchasing.",
      features: [
        "Personalized Recommendations",
        "One-Click Reordering",
        "Virtual Try-On Technology",
      ],
    },
    {
      name: "Fashionista85",
      review:
        "Basket's virtual try-on feature is amazing! I love being able to see how different outfits look on me before making a purchase. Plus, the quick delivery option is a lifesaver when I need something urgently.",
      features: ["Virtual Try-On Technology", "Quick Delivery Option"],
    },
    {
      name: "TechieGuy2023",
      review:
        "As a tech enthusiast, I appreciate Basket's user-friendly interface and smooth navigation. The advanced search functionality helps me find specific products quickly, and the integration with multiple payment gateways ensures a secure transaction every time.",
      features: [
        "User-Friendly Interface",
        "Advanced Search Functionality",
        "Multiple Payment Gateways",
      ],
    },
    {
      name: "EcoFriendlyMom",
      review:
        "Basket's eco-friendly product filter is a game-changer for me! I can easily find sustainable and environmentally-friendly options for my family. Additionally, the wishlist feature helps me keep track of items I plan to purchase in the future.",
      features: ["Eco-Friendly Product Filter", "Wishlist Feature"],
    },
    {
      name: "Shopaholic92",
      review:
        "One-click reordering is a game-changer! I can quickly restock my essentials without any hassle. Basket saves me so much time! Additionally, the advanced search filters make it easy to narrow down exactly what I'm looking for, and the secure payment options give me peace of mind when making purchases",
      features: [
        "One-Click Reordering",
        "Advanced Search Filters",
        "Secure Payment Options",
      ],
    },
  ];
</script>

<SectionWrapper id>
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex 1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Don't just take our word for it
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        See What <span class="text-indigo-400">Others</span>Have To Say
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? ReviewsList.slice(0, 4) : ReviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>
      <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each lim ? ReviewsList.slice(0, 4) : ReviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtn">
      <p>{lim ? "Show More" : "Show Less"}</p>
    </button>
    <div class="flex flex-col gap-10">
      <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
        Trusted by 1,349 Swoldiers
      </p>
      <!-- <Stars /> -->
    </div>
  </div></SectionWrapper
>
