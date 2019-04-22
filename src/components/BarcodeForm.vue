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
    <button v-on:click="updateMainList">Create</button>
    <button v-on:click="clearList">Clear</button>
  </form>
</template>

<script>
export default {
  name: "BarcodeForm",
  data() {
    return {
      list: "",
      listSplit: "",
      trimmedList: [],
      test: "1"
    };
  },
  methods: {
    createList() {
      this.listSplit = this.list.split("\n");
      this.trimList(this.trimmedList);
    },
    trimList() {
      for (let i = 0; i < this.listSplit.length; i++) {
        this.trimmedList[i] = this.listSplit[i].trim();
      }
    },
    clearList() {
      this.list = "";
      this.listSplit = "";
      this.trimmedList = [];
    },
    updateMainList: function() {
      this.createList();
      this.$emit("updatedList", this.trimmedList);
    }
  }
};
</script>

<style></style>
