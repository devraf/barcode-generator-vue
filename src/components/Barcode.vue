<template>
  <li>
    {{ letter }}
  </li>
</template>

<script>
export default {
  name: "Barcode",
  data() {
    return {
      letter: "mybarcode"
    };
  }
};
</script>

<style scoped></style>
