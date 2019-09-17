<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About"
      subtitle="If you were wondering..."
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Lifestyle blog</h3>
          <p>
            This is a lifestyle blog on which you can find experiences,
            learnings and recommendations on various topics and products that
            aim to improve your physical and mental well-being.
          </p>
          <p>
            Feedback, opinions and any constructive engagement here is very
            welcome!
          </p>
          <h3>The inspiration</h3>
          <p>
            After a personally transformative year I've decided to start sharing
            my learnings about various topics such as: diets, fitness, health,
            procrastination, smoking and alcohol.
          </p>

          <h3>The motivation</h3>
          <p>
            I want to share my experiences and learnings to positively influence
            you to make the best choices for yourself when it comes to your
            well-being.
          </p>
          <quote-card />
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
