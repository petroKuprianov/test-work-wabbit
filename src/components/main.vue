<template>
<div class="main">
  <div class="main_info">
    <div class="main_info_icon">
      <img src="../assets/mail.png" alt="mail img">
    </div>
    <div class="main_info_desc">
      <div class="main_info_desc-header">
        Более 569 клиентов уже написали нам
      </div>
      <div class="main_info_desc_info">
        <input type="text" class="main_info_desc_info-input" placeholder="Напишите ваш email">
        <button class="main_info_desc_info-btn">Отправить</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
name: "main"
}
</script>

<style scoped>

.main{
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 150px;
}
.main_info{
  width: 1110px;
  height: 288px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: no-repeat url("../assets/BG_Mask.png");
}

.main_info_desc-header{
  width: 445px;
  font-family: Inter;
  font-style: normal;
  font-weight: 800;
  font-size: 40px;
  line-height: 54px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #FFFFFF
}

.main_info_desc{
  margin-left: 122px;
}
.main_info_desc_info{
  display: flex;
  align-items: center;
  margin-top: 32px;
}

.main_info_desc_info-input{
  display: flex;
  align-items: center;
  border: none;
  padding: 0 0 0 16px;
  width: 248px;
  height: 52px;

  background: #F4F5F7;
  border-radius: 5px 0px 0px 5px;

}

.main_info_desc_info-btn{
  width: 123px;
  height: 52px;
  cursor: pointer;
  background: #18191F;
  border-radius: 0px 5px 5px 0px;
  border: none;
  padding: 14px 24px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #FFFFFF;
}
</style>
