<template>
  <b-alert class="mt-5" variant="dark" show>Você está offline =(</b-alert>
</template>

<script>
import NNotaVue from './NNota.vue';
export default {
  name: "offline-alert",
 props: {
    id: [NNotaVue]
  },
  data() {
    return {
      NNotaVue = NNotaVue
    };
  },
  methods: {
    recarregar() {
        this.$fetch()
      }
    }
};
 
</script>

<style></style>
