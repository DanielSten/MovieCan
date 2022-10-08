<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "tab-button"
}
</script>

<style scoped>
*{
border: 0px;
}
button{
  padding: 20px 50px;
  width: 350px;
  border-bottom: 2px solid #985EFF;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #985EFF;
  background-color: white;
}
button.active{
  padding-bottom: 22px;
  color: rgba(86, 0, 232, 1);
  border: 2px solid #985EFF;
  border-bottom: none;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}
</style>