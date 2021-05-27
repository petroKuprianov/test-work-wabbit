<template>
  <div class="news">
    <h3 class="news_header">Новости</h3>
    <div class="news_items_first">
      <img :src="require( `../assets/${news[0] ? news[0].ID : '47933'}.png`)" alt="">
      <div class="news_items_first_info">
        <div class="news_items_first_info-wrapper">
          <span class="news_items_first_info-heading">SEO</span>
          <img src="../assets/Line.png" alt="line img">
          <span class="news_items_first_info-time">5 мин чтения</span>
        </div>
        <div class="news_items_first_info-content">
          <h4 v-html="news[0] ? news[0].NAME : ''"></h4>
          <div v-html="news[0]? news[0].PREVIEW_TEXT : ''" class="news_items_first_info-content-desc"></div>
          <div class="news_items_first_info-content-btn">
            <a href="#">
              Подробнее
              <img src="../assets/Vector_pink.png" alt="Vector img">
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="news_items">
      <splide>
        <splide-slide v-for="(item) in news" :key="item.ID" class="new_items_item">
          <div class="new_items_item-img">
            <img :src="require( `../assets/${item.ID}.png`)" alt="">
          </div>
          <div class="news_items_first_info-wrapper">
            <span class="news_items_first_info-heading">SEO</span>
            <img src="../assets/Line.png" alt="line img">
            <span class="news_items_first_info-time">5 мин чтения</span>
          </div>
          <div  v-html="item.NAME" class="new_items_item-name"></div>
        </splide-slide>
      </splide>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { Splide, SplideSlide } from '@splidejs/vue-splide';
// import {VueGlide, VueGlideSlide} from 'vue-glide-js'
// import VueGlide from '@vue-glide-js/src/components/Glide.vue'
// import VueGlideSlide from '@vue-glide-js/src/components/GlideSlide.vue'
import '@splidejs/splide/dist/css/themes/splide-default.min.css';


export default {
  name: "news",
  components:{
    Splide,
    SplideSlide,
  },
  data() {
    return {
      news: []
    }
  },
  mounted() {
    this.loadAsyncData()
  },
  methods:{
    async loadAsyncData() {
      await axios('https://b24crm-nst.s11.itua.in.ua/rest/513/tz8j9hozz843f81k/lists.element.get.json?IBLOCK_TYPE_ID=lists&IBLOCK_ID=153&ELEMENT_ORDER%5bID%5d=DESC',{
        method: 'GET'
      })
          .then((res) => {
            this.news = res.data.result
            console.log(this.news);
          })
    }
  }
}
</script>


<style scoped>
.news{
  padding-left: 165px;
}
.news_header{
  font-family: Inter;
  font-style: normal;
  font-weight: 800;
  font-size: 48px;
  line-height: 64px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}

.news_items_first{
  display: flex;
  align-items: center;
}

.news_items_first_info-wrapper{
  display: flex;
  align-items: center;
}
.news_items_first_info-wrapper img{
  margin-left: 10px;
}
.news_items_first_info{
  margin-left: 30px;
}
.news_items_first_info-heading{
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 12px;
  letter-spacing: 1px;
  color: #8C30F5;
}

.news_items_first_info-time{
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 12px;
  letter-spacing: 0.5px;
  color: #18191F;
  mix-blend-mode: normal;
  opacity: 0.3;

  margin-left: 10px;
}


.news_items_first_info-content h4{
  font-family: Inter;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 130%;
  color: #18191F;
}

.news_items_first_info-content-desc{
  height: 172px;
  overflow: hidden;
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 160%;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #18191F;
}
.news_items_first_info-content-btn{
  margin-top: 24px;
}
.news_items_first_info-content-btn a{
  text-decoration: none;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 16px;
  font-feature-settings: 'salt' on, 'liga' off;
  color: #8C30F5;
}

.new_items_item{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.new_items_item-img{
  margin-top: 60px;
  margin-bottom: 30px;
}
.new_items_item-name{
  margin-bottom: 30px;
  font-family: Inter;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 130%;
  color: #18191F;
}
</style>
