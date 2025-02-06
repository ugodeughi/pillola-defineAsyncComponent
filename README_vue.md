# 🚀 Pillole di Web Dev – `defineAsyncComponent` in Vue 3

⚡ **Caricare componenti in modo asincrono** è utile per ottimizzare il caricamento delle pagine, riducendo il peso iniziale del bundle. In **Vue 3**, possiamo usare `defineAsyncComponent` per **lazy-load dei componenti** solo quando servono.

## 🏗️ Sintassi Base con `<script setup>`

```vue
<script setup>
import { defineAsyncComponent } from 'vue';

// Caricamento asincrono del componente
const MyLazyComponent = defineAsyncComponent(() => import('@/components/MyLazyComponent.vue'));
</script>

<template>
  <div>
    <h2>📌 Caricamento Asincrono</h2>
    <MyLazyComponent />
  </div>
</template>
```

## 🕵️‍♂️ Gestire il Fallback e gli Errori

Puoi aggiungere un **fallback** durante il caricamento e un componente per gli **errori**:

```vue
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
  <div>
    <h2>🚀 Lazy Loading Avanzato</h2>
    <MyLazyComponent />
  </div>
</template>
```

## 📌 Perché usarlo?
✅ Riduce il **tempo di caricamento iniziale**  
✅ Carica il componente **solo quando necessario**  
✅ **Migliora la UX** con fallback durante l’attesa  

🔹 **Usalo per componenti secondari**, come modali, grafici o elementi complessi!

---

🔗 **Seguimi su [pillolewebdev.it](https://pillolewebdev.it) per altre pillole!** 🚀  

**#VueJs #Vue3 #LazyLoading #Performance #UgoDeUghi #PilloleDiWebDev**
