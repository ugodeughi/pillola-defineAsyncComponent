<script setup>
import { defineAsyncComponent } from 'vue';

const MyLazyComponent = defineAsyncComponent({
  loader: () => import('@/components/MyLazyComponent.vue'),
  loadingComponent: defineAsyncComponent(() => import('@/components/LoadingSpinner.vue')),
  errorComponent: defineAsyncComponent(() => import('@/components/ErrorComponent.vue')),
  delay: 200, // Mostra il fallback dopo 200ms
  timeout: 3000 // Timeout dopo 3s
});
</script>

<template>
  <main>
    <div>
      <h2>Lazy Loading</h2>
      <MyLazyComponent />
    </div>
  </main>
</template>