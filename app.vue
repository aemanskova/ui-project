<template>
  <div>
    <div class="wrap">
      <section>
        <Navbar />
        <Banner />
      </section>

      <section class="section">
        <SitesExamples />
      </section>
      <section class="section">
        <Technology />
      </section>
      <section class="section">
        <Tasks></Tasks>
      </section>
      <section class="section">
        <StrategyBlock></StrategyBlock>
      </section>
      <section class="section">
        <SliderOverflowBlock></SliderOverflowBlock>
      </section>
      <section class="section">
        <GalleryBlock />
      </section>

      <section class="section">
        <MotivationCard
          color="var(--white)"
          img
          header="Вы получите не просто бренд, а образ жизни, к которому стремитесь"
          text="Наша технология сделает дело вашей жизни или проект в инвестпортфеле успешным"
        >
          <template v-slot:img>
            <img src="/img/suit.png" alt="" />
          </template>
        </MotivationCard>
      </section>
      <section class="section">
        <ServicesBlock />
      </section>
      <section class="section">
        <SeeWithUsBlock />
      </section>
      <section class="section">
        <InvitationBlock />
      </section>
    </div>
    <section class="section section--last">
      <Footer />
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      link: [
        { rel: "preconnect", href: "https://fonts.googleapis.com" },
        {
          rel: "preconnect",
          href: "https://fonts.gstatic.com",
          crossorigin: true,
        },
        {
          rel: "stylesheet",
          href: "https://fonts.googleapis.com/css2?family=Onest:wght@400;500&display=swap",
        },
        {
          rel: "stylesheet",
          href: "/assets/globals.css",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap {
  padding: 16px;
  max-width: 1920px;
  margin: 0 auto;
}
.section {
  margin-top: 80px;
  &--last {
    background-color: var(--bg-footer);
    padding: 16px;
    border-radius: 10px 10px 0 0;
  }
}
img {
  object-fit: cover;
  width: 100%;
  border-radius: 10px;
}
@media (min-width: 768px) {
  .wrap {
    padding: 20px 40px;
  }
  .section {
    margin-top: 120px;
    &--last {
      padding: 20px 40px;
    }
  }
}
@media (min-width: 1440px) {
  .wrap {
    padding: 30px 160px;
  }
  .section {
    margin-top: 220px;
    &--last {
      padding: 30px 160px;
    }
  }
}
</style>