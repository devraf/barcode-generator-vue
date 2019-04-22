<template>
  <main>
    <h1>hi</h1>
    <BarcodeForm v-on:updatedList="makeNewList" />
    <ul v-for="(item, index) in list" v-bind:key="index">
      <Barcode v-bind:text="item" />
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
  },
  data() {
    return {
      list: []
    };
  },
  methods: {
    makeNewList(arg) {
      this.list = arg;
    }
  }
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
