<script>
import axios from "axios";

export default {
  data() {
    return {
      cardList: [],
    };
  },
  methods: {
    fetchCards() {
      axios
        .get(
          "https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Alien&num=20&offset=0"
        )
        .then((res) => {
          let cardResults = res.data.data;
          //   console.log(cardResults);
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
  <div class="row row-cols-lg-6 d-flex justify-content-around">
    <div class="col mx-1 mb-4 ms-Card text-center" v-for="card in cardList">
      <img src="" alt="" />
      <h6>{{ card.name }}</h6>
      <p>{{ card.archetype }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.ms-Card {
  background-color: orange;
  color: white;
  img {
    width: 100%;
  }
}
</style>
