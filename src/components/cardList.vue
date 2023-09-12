<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Hello world",
    };
  },
  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((res) => {
        console.log(res);
      });
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style lang="scss" scoped></style>
