# 🚀 Componenti per `defineAsyncComponent` in Vue 3

Questo repository contiene tre componenti per la gestione del caricamento asincrono con `defineAsyncComponent` in Vue 3.

## 📌 MyLazyComponent.vue
Questo è il componente principale che viene caricato in modo asincrono.

```vue
<template>
  <div class="p-4 bg-success text-white rounded">
    <h3>✅ MyLazyComponent Caricato!</h3>
    <p>Questo componente è stato caricato in modo asincrono.</p>
  </div>
</template>

<script setup>
// Puoi aggiungere eventuale logica qui
</script>

<style scoped>
/* Stile di esempio */
</style>
```

---

## 🔄 LoadingSpinner.vue
Questo componente viene mostrato mentre `MyLazyComponent` è in fase di caricamento.

```vue
<template>
  <div class="d-flex justify-content-center align-items-center p-4">
    <div class="spinner-border text-primary" role="status">
      <span class="visually-hidden">Caricamento...</span>
    </div>
    <p class="ms-2">Caricamento in corso...</p>
  </div>
</template>

<script setup>
// Nessuna logica necessaria
</script>

<style scoped>
/* Lo stile Bootstrap viene usato per la spinner */
</style>
```

---

## ❌ ErrorComponent.vue
Questo componente viene mostrato se il caricamento di `MyLazyComponent` fallisce.

```vue
<template>
  <div class="p-4 bg-danger text-white rounded">
    <h3>❌ Errore nel caricamento!</h3>
    <p>Si è verificato un errore durante il caricamento del componente.</p>
  </div>
</template>

<script setup>
// Eventuale gestione degli errori
</script>

<style scoped>
/* Stile di esempio */
</style>
```

---

## 📌 Come Funziona
- Se il caricamento di `MyLazyComponent` richiede più di **200ms**, verrà mostrato `LoadingSpinner.vue`.
- Se il caricamento supera i **3 secondi** o fallisce, apparirà `ErrorComponent.vue`.

---

🔗 **Seguimi su [pillolewebdev.it](https://pillolewebdev.it) per altre pillole!** 🚀  

**#VueJs #Vue3 #LazyLoading #Performance #UgoDeUghi #PilloleDiWebDev**
