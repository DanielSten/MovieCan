<template>
  <div class="flex nav">
    <div class="nav_logo"><RouterLink to="/"><img src="./icons/logo.png"></RouterLink></div>
    <div class="nav_name"><RouterLink to="/">MovieCan</RouterLink></div>
    <div class="nav_icon_account"><RouterLink to="/"><img src="./icons/icon_account.png"></RouterLink></div>
  </div>
</template>

<script>
export default {
  name: "nav-menu"
}
</script>

<style scoped>
.flex{
  display: flex;
  align-items:center;
}
.nav{
  background-color: #7F39FB;
  height: 75px;
  width: 100%;
  padding: 0 25px;
}
.nav_logo{
  margin-right: 15px;
}
.nav_logo img{
  height: 40px;
  width: 40px;
}
.nav_name a{
  font-weight: 500;
  font-size: 36px;
  line-height: 24px;
  letter-spacing: 0.15px;
  -webkit-text-stroke: 1px #000000;
  color: #F2E7FE;
}
.nav_icon_account{
  position: absolute;
  right: 25px;
}
</style>