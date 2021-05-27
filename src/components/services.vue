<template>
<div class="services">
  <h3 class="services_header">Наши услуги</h3>
  <div class="services_wrapper">
    <div class="services_content">
      <div class="services_item" v-for="(item, index) in services" :key="item.ID" :class="index === 0 ? 'services_item-first' : 'services_item-notFirst'">
        <img class="services_item-bg" :src="require( `../assets/${item.ID}.png`)" alt="img">
        <div class="services_item-name" :class="index === 0 ? 'services_item-name-first' : 'services_item-name-notFirst'">{{item.NAME}}</div>
        <div v-if="index === 0" v-html="item.PREVIEW_TEXT" class="services_item-desc"></div>
        <div v-if="index === 0" class="services_item-btn">
          <a href="#">
            Подробнее
            <img src="../assets/Vector_pink.png" alt="Vector img">
          </a>
        </div>
      </div>
    </div>
    <button class="services-btn">
      Связаться с нами
      <img src="../assets/Vector_black.png" alt="Vector img">
    </button>
  </div>
</div>
</template>

<script>
import axios from 'axios'


export default {
  name: "services",
  data() {
    return{
      services: [],
      images: {}
    }
  },
  mounted() {
    this.loadAsyncData()

  },
  methods: {
    async loadAsyncData() {
      await axios('https://b24crm-nst.s11.itua.in.ua/rest/513/tz8j9hozz843f81k/lists.element.get.json?IBLOCK_TYPE_ID=lists&IBLOCK_ID=152&ELEMENT_ORDER%5bID%5d=ASC',{
        method: 'GET'
      })
          .then((res) => {
            this.services = res.data.result
          })
    }
  }
}
</script>

<style scoped>
.services{
  width: 100%;
  background: #F4F5F7;
  padding-top: 150px;
}

.services_header{
  font-family: Inter;
  font-style: normal;
  font-weight: 800;
  margin: 0 0 48px 0;
  font-size: 48px;
  line-height: 64px;
  text-align: center;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}
.services_wrapper{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.services_content{
  display: grid;
  grid-template-columns: repeat(3, 350px);
  grid-template-rows: 382px 382px;
  grid-column-gap: 30px;
  grid-row-gap: 75px;
}

.services_item{
  width: 290px;
  height: 346px;
  background: #FFFFFF;
  backdrop-filter: blur(4px);
  border-radius: 3px;
}
.services_item-bg{
  position: absolute;
  top:0;
  left: 0;
  z-index: -1;
  height: inherit;
  object-fit: cover;
  border-radius: 3px;
}
.services_item-notFirst{
  display: flex;
  align-items: flex-end;
}

.services_item-name-notFirst{
  margin-bottom: 40px;
}

.services_item-name{
  font-family: Inter;
  font-style: normal;
  margin-left: 32px;
  font-weight: 600;
  font-size: 24px;
  line-height: 32px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}

.services_item-desc{
  max-width: 286px;
  margin-left: 32px;
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 26px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;

}

.services_item-name-first{
  margin-top: 128px;
}

.services_item-btn{
  margin-top: 20px;
  margin-left: 32px;
  margin-bottom: 40px;
}
.services_item-btn a{
  text-decoration: none;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 16px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #8C30F5;
}

.services-btn{
  width: 221px;
  height: 48px;
  border: 1px solid #18191F;
  box-sizing: border-box;
  border-radius: 6px;

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;

  margin-top: 48px;
  margin-bottom: 150px;

  cursor: pointer;
}

</style>
