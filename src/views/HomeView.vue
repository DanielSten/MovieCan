<template>
  <div>
    <Slider></Slider>
    <div class="container">
      <TabButton :class="{active: isTabActive(0)}" @click="onTabClick(0)">Рекомендовано вам</TabButton>
      <TabButton :class="{active: isTabActive(1)}" @click="onTabClick(1)">Новинки</TabButton>
      <TabButton :class="{active: isTabActive(2)}" @click="onTabClick(2)">Самые просматриваемые</TabButton>
      <div class="tabs_body">
        <div class="tab_body" v-show="isTabActive(0)">
          <CardListRecommend></CardListRecommend>
        </div>
        <div class="tab_body" v-show="isTabActive(1)">
          <CardListRecommend></CardListRecommend>
        </div>
        <div class="tab_body" v-show="isTabActive(2)">
          <CardListRecommend></CardListRecommend>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Slider from "../components/slider.vue";
import CardFilm from "../components/card-film.vue";
import CardListRecommend from "../components/card-list-recommend.vue";
import TabButton from "../components/tab-button.vue";

export default {
  components: {
    Slider,
    CardFilm,
    CardListRecommend,
    TabButton,
  },
  data() {
    return{
    tabActive: 0,
    }
  },
  methods: {
    isTabActive(num){
      return this.tabActive === num;
    },
    onTabClick(num){
      this.tabActive = num;
    }
  },
}

</script>

<style scoped>

.container {
  margin: 24px auto;
  max-width: 1440px;
}
.tabs_body{
  margin-top: 25px;
}

</style>


