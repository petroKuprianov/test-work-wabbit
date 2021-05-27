<template>
<div class="about">
  <div class="about_bg"></div>
  <div class="about_bg_content">
    <h2 class="about_bg_content-header">Делаем больше чем просто SEO</h2>
    <div class="about_bg_content-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc odio in et, lectus sit lorem id integer.</div>
    <button class="about_bg_content-button">Связаться с нами</button>
  </div>
</div>
</template>

<script>
export default {
  name: "about"
}
</script>

<style scoped>
.about{
  width: 100%;
  height: 780px;
  max-height: 780px;
}
.about_bg{
  width: 100%;
  position: relative;
  top: 0;
  height: inherit;
  float: right;
  z-index: -1;
  background: no-repeat url("../assets/image_bg.png");
  background-size: cover;
}

.about_bg_content{
  max-width: 635px;
  max-height: 350px;
  position: absolute;
  top: 176px;
  left: 166px;
  z-index: 30;
}
.about_bg_content-header{
  font-family: Inter;
  font-style: normal;
  font-weight: 800;
  font-size: 72px;
  line-height: 98px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}
.about_bg_content-text{
  max-width: 540px;
  margin-top: 16px;
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 32px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}
.about_bg_content-button{
  width: 205px;
  height: 48px;
  cursor: pointer;
  border: none;
  background: #8C30F5;
  border-radius: 6px;
  margin-top: 32px;

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #FFFFFF;
}

@media screen and (max-width: 1440px){
.about_bg{
width: 100%;
height: inherit;
float: right;
background: no-repeat url("../assets/image_bg.png");
background-size: contain;
}
}

</style>
