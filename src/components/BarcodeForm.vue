<template>
  <form v-on:submit.prevent v-on:enter.prevent>
    <label for="list">Add list</label>
    <textarea
      v-model="list"
      name="list"
      id="list"
      cols="30"
      rows="10"
    ></textarea>
    <button v-on:click="createList">Create</button>
    <button>123</button>
  </form>
</template>

<script>
export default {
  name: "BarcodeForm",
  data() {
    return {
      list: "",
      listArray: []
    };
  },
  methods: {
    createList() {
      console.log(this.list.trim());

      // this.listArray.push(this.list.split("\n"));
      // return this.listArray.push(this.list);
    }
  }
};
</script>

<style></style>
