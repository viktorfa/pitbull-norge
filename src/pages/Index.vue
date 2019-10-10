<template>
  <Layout>
    <div id="main-page">
      <div id="landing-hero-full">
        <div>
          <p class="text-header text-hero text-uppercase">
            Pitbull 🌎
            <br />Fanklubb
            <br />Norge 🇳🇴
          </p>
        </div>
        <div class="flex justify-between">
          <div>
            <g-image src="~/assets/images/p-logo.svg" width="50" />
          </div>
          <div class="flex justify-center w-full text-2xl">
            <div>Hvem –&nbsp;</div>
            <div>Hva –&nbsp;</div>
            <div>Hvorfor</div>
          </div>
          <div class="invisible">Dale!</div>
        </div>
      </div>
      <!-- END LANDING FULL -->
      <div id="quote" class="flex">
        <div class="w-1/2 m-2">
          <g-image src="~/assets/images/pitbull-weird.jpg" />
        </div>
        <div class="w-1/2 m-2">{{quote}}</div>
      </div>
    </div>
    <!-- END MAIN -->
  </Layout>
</template>

<script>
const getPitbullQuotes = () => [
  "Every day above ground is a good day. Dale!",
  "Let it rain over me!",
  "I can't promise tomorrow. But I can promise tonight. Dale!",
  "¡No pare la fiesta! Don't stop the paaarty!",
  "That's why they call me Mr WorldWide!",
  "Taking my life from negative to positive.",
  "Picture that with a Kodak®. Or better yet, go to times square. And take a picture of me with a Kodak®.",
];
export default {
  metaInfo: {
    title: "Mr WorldWide!",
  },
  data() {
    return { quotes: getPitbullQuotes() };
  },
  computed: {
    quote() {
      return this.quotes[Math.floor(Math.random() * this.quotes.length)];
    },
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
