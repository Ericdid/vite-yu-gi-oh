<script>
import axios from "axios";

export default {
  data() {
    return {
      title: "Hello world",
      cardList: [],
    };
  },
  methods: {
    fetchCards() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then((res) => {
          let cardResults = res.data.data;
          // console.log(cardResults);
          this.cardList = cardResults;
        });
    },
  },

  created() {
    this.fetchCards();
  },
};
</script>

<template>
  <div class="row row-cols-lg-5">
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
    <div class="col">card</div>
  </div>
</template>

<style lang="scss" scoped></style>
