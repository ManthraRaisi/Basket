<script>
  import SectionWrapper from "./SectionWrapper.svelte";
  let faqs = [
    {
      question: "What is Basket?",
      answer:
        "Basket is a web application designed for selling products online, similar to platforms like Amazon. It allows users to browse through various products, add items to their shopping cart, and proceed to checkout to make purchases.",
    },
    {
      question: "What features does Basket offer?",
      answer:
        "Basket offers a range of features including personalized recommendations, one-click reordering, virtual try-on technology, advanced search filters, secure payment options, and more.",
    },
    {
      question: "How does Basket's personalized recommendations work?",
      answer:
        "Basket employs advanced algorithms to analyze users' browsing and purchase history, providing tailored product recommendations based on their preferences and behavior.",
    },
    {
      question: "Is Basket's checkout process secure?",
      answer:
        "Yes, Basket ensures a secure checkout process by integrating with multiple payment gateways and implementing industry-standard security measures to protect users' payment information.",
    },
    {
      question: "Can I track my orders on Basket?",
      answer:
        "Absolutely! Basket provides order tracking functionality, allowing users to monitor the status of their orders and receive updates on shipping and delivery.",
    },
    {
      question: "Does Basket offer customer support?",
      answer:
        "Yes, Basket provides customer support services to assist users with inquiries, returns, and other issues. You can reach out to our support team via email, live chat, or phone.",
    },
    {
      question: "Are there any subscription fees for using Basket?",
      answer:
        "Basket is free to use for browsing and purchasing products. However, some premium features or subscription-based services may incur additional fees.",
    },
    {
      question: "Can I return items purchased through Basket?",
      answer:
        "Yes, Basket has a return policy that allows users to return items within a specified period for a refund or exchange. Please refer to our returns policy for more information.",
    },
    {
      question: "Does Basket offer international shipping?",
      answer:
        "Yes, Basket offers international shipping to select countries. Shipping rates and delivery times may vary depending on the destination.",
    },
    {
      question: "How can I update my account information on Basket?",
      answer:
        "You can update your account information, including your shipping address and payment details, by accessing your account settings on the Basket website or app.",
    },
    {
      question: "Can I sell products on Basket as a seller?",
      answer:
        "At the moment, Basket is a platform for purchasing products rather than selling. However, if you're interested in selling your products, you can explore other e-commerce platforms or marketplaces.",
    },
    {
      question: "Is my personal information secure on Basket?",
      answer:
        "Yes, Basket takes user privacy and security seriously. We employ industry-standard security measures to protect users' personal information and use encryption to secure data transmission.",
    },
    {
      question: "Does Basket have a mobile app?",
      answer:
        "Yes, Basket offers a mobile app for both iOS and Android devices, providing users with a convenient way to shop on the go.",
    },
    {
      question: "Can I save items for later on Basket?",
      answer:
        "Yes, Basket provides a 'Save for Later' feature, allowing users to bookmark items they're interested in but not ready to purchase yet. You can access your saved items from your account.",
    },
    {
      question: "Does Basket offer discounts or promotions?",
      answer:
        "Yes, Basket occasionally runs promotions and offers discounts on select products. Be sure to sign up for our newsletter or follow us on social media to stay updated on the latest deals.",
    },
  ];
</script>

<SectionWrapper id="faqs">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For all your questions, qualms & queries
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Frequently Asked Questions
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
            {faq.question}
          </h4>
          <p class="pl-2">{faq.answer}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
