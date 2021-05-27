<template>
<div class="header">
  <div class="header_nav">
    <a href="#">
      <img class="header_nav-logo" src="../assets/logo.png" alt="Logo">
    </a>
    <div class="header_nav_items">
      <div class="header_nav_item">
        <a href="#">О нас</a>
      </div>
      <div class="header_nav_item">
        <a href="#">Почему мы</a>
      </div>
      <div class="header_nav_item">
        <a href="#">Наши услуги</a>
      </div>
      <div class="header_nav_item">
        <a href="#">Новости</a>
      </div>
    </div>
  </div>
  <div class="header_info">
    <div class="header_info_phone">
      <img src="../assets/Call.png" alt="Call img">
      <span class="header_info_phone-number">067-777-00-00</span>
    </div>
    <div class="header_info_btn">
      <button>Связаться с нами</button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "header"
}
</script>

<style scoped>

.header{
  width: calc(100% - 330px);
  height: 72px;
  padding: 0 165px 0 165px;
  display: flex;
  align-items: center;
  background: #FFFFFF;
  box-shadow: 0px 1px 0px #E5E9F2;
}
.header_nav{
  display: flex;
}
.header_nav_items{
  display: flex;
  align-items: center;
}
.header_nav_item{
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  margin-left: 32px;
}
.header_nav_item a{
  text-decoration: none;
  color: #18191F;
}

.header_info{
  display: flex;
  align-items: center;
  margin-left: auto;
}
.header_info_phone{
  height: fit-content;
}

.header_info_phone-number{
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #8C30F5;
  margin-left: 8px;
}

.header_info_btn{
  margin-left: 32px;
}
.header_info_btn button{
  cursor: pointer;
  width: 163px;
  height: 40px;
  border: none;
  padding: 10px 20px;
  background: #8C30F5;
  border-radius: 6px;

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  color: #FFFFFF;

}

</style>
