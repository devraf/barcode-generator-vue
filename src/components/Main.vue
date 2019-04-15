<template>
  <main>
    <h1>hi</h1>
    <BarcodeForm />
  </main>
</template>

<script>
import BarcodeForm from "@/components/BarcodeForm.vue";

export default {
  name: "Main",
  components: {
    BarcodeForm
  }
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
