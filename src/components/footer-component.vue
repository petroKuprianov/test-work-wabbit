<template>
  <div class="footer">
    <div class="footer_wrapper">
      <a href="#">
        <img src="../assets/logo_2.png" alt="Logo img">
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
      <img class="footer_divider" src="../assets/Divider.png" alt="img">
      <div class="footer_bottom">
        <div class="footer_bottom_copy">© 2021 Wabbit. All rights reserved</div>
        <div class="footer_bottom_social">
          <a href="#" class="footer_bottom_social-item">
            <img src="../assets/insta.png" alt="insta img">
          </a>
          <a href="#" class="footer_bottom_social-item">
            <img src="../assets/Path.png" alt="insta img">
          </a>
          <a href="#" class="footer_bottom_social-item">
            <img src="../assets/twitter.png" alt="insta img">
          </a>
          <a href="#" class="footer_bottom_social-item">
            <img src="../assets/youtube.png" alt="insta img">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: "footer-component"
}
</script>

<style scoped>
.footer{
  width: 100%;
  height: 310px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  align-items: center;
  background: #0B0D17;
  margin-top: 150px;
}
.footer_wrapper{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.header_nav_items{
  display: flex;
  align-items: center;
  margin-top: 20px;
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

  color: #FFFFFF;
}

.footer_divider{
  margin-top: 75px;
}
.footer_bottom{
  width: 1110px;
  display: flex;
  justify-content: space-between;
  margin-top: 12px;
}
.footer_bottom_copy{
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 24px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #D9DBE1;
}

.footer_bottom_social{
  width: 144px;
  display: flex;
}

.footer_bottom_social-item{
  width: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 16px;
  border-radius: 100%;
  background: #18191F;
}
</style>
