<template>
  <main>
    <TInput></TInput>
    <TCard></TCard>
  </main>
</template>

<script>
import TCard from "./components/TCard.vue";
import TInput from "./components/TInput.vue";

export default {
  name: 'App',
  components: {
    TCard,
    TInput
  }
}
</script>
