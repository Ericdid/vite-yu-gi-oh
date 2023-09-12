<script>
import cardList from "./cardList.vue";

export default {
  data() {
    return {
      title: "",
    };
  },
  components: { cardList },
};
</script>

<template>
  <section class="main-section">
    <div class="container">
      <select class="select pe-5 p-1 mt-3">
        <option value="alien">Alien</option>
      </select>
      <div class="card-cont mt-2">
        <div class="container card-founded"><strong>found x card</strong></div>
        <div class="row row-cols-lg-5">
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <div class="col">card</div>
          <cardList />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.main-section {
  height: 900px;
  background-color: orange;
  .select {
    border-radius: 5px;
  }
  .card-cont {
    height: 800px;
    background-color: white;

    .card-founded {
      width: 100%;
      height: 5%;
      background-color: black;
      color: white;
      display: flex;
      align-items: center;
    }
  }
}
</style>
