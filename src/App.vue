<template>
  <div id="app" class="flex flex-col min-h-screen bg-gray-700 text-white">
    <!-- Scrollable main content -->
    <main class="flex overflow-auto pb-32 md:pb-24">
      <PortfolioSection />
    </main>

    <!-- Fixed Footer -->
    <Footer />
  </div>
</template>

<script>
import PortfolioSection from './components/PortfolioSection.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    PortfolioSection,
    Footer
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Inter', sans-serif;
}
</style>
