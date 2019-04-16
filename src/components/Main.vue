<template>
  <main>
    <h1>hi</h1>
    <BarcodeForm />
    <ul>
      <Barcode />
    </ul>
  </main>
</template>

<script>
import BarcodeForm from "@/components/BarcodeForm.vue";
import Barcode from "@/components/Barcode.vue";

export default {
  name: "Main",
  components: {
    BarcodeForm,
    Barcode
  }
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
