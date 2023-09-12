<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Hello world",
      cardList: [],
    };
  },
  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((res) => {
        let cardResults = res.data.data;
        // console.log(cardResults);
        this.cardList = cardResults;
      });
  },
};
</script>

<template></template>

<style lang="scss" scoped></style>
