<template>
  <div>
    <Header />
    <main>
      <NuxtPage />
    </main>
    <Footer />
  </div>
</template>
  
  <script>
import Header from "~/components/Header.vue";

export default {
  components: {
    Header
  }
};
</script>
  
  <style scoped>
/* استایل‌های مربوط به layout */
</style>
  