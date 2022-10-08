<template>
  <div>
    <div class="buttons">
      <div
          class="button"
          v-for="tab in tabs"
          :key="tab"
          :class="['tab-button', { active: currentTab === tab }]"
          @click="currentTab = tab"
      >
        {{ tab }}
      </div>
    </div>
    <component :is="currentComponent" class="tab"></component>
  </div>
</template>

<script>
import CardListRecommend from "./card-list-recommend.vue";
import CardListNew from "./card-list-new.vue";
import CardListPopular from "./card-list-popular.vue";

export default {
  name: "tabs",
  components: {
    CardListRecommend,
    CardListNew,
    CardListPopular
  },
  props: ['title'],
  data() {
    return {
      tabs: ['CardListRecommend', 'Новинки', 'Самые просматриваемые'],
      currentTab: 'CardListRecommend',
    }
  },
  computed: {
    currentComponent() {
      return `card-list-${this.currentTab}`
    }
  },
}
</script>

<style scoped>
.buttons{
  padding-top: 25px;
  display: flex;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #985EFF;
  text-align: center;
}
.button{
  padding: 20px 50px;
  width: 350px;
  border-bottom: 2px solid #985EFF;
}
.button.active{
  color: rgba(86, 0, 232, 1);
  border: 2px solid #985EFF;
  border-bottom: 0;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}
.tab{
  padding: 10px;
}
</style>