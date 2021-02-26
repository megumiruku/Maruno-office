<template>
  <div class="main">
    <!------------------
     ----Firstview---
     ----------------->-
    <div class="eyecatch">
        <img src="../assets/first-view.jpg" alt="" />
    </div>
    <!--------------
     -----Service----- 
     ----------------->
    <div class="service mg-80">
      <h1 class="section-ttl">サ－ビス</h1>
      <div class="service-wrap" >
        <div class="service-card" v-for="(data, index) in service" :key="index" @click="link()">
          <img :src="data.img" :alt="data.alt" />
          <h2 class="service-card-ttl">{{data.ttl}}</h2>
          <p class="service-card-content">{{data.description}}</p>
        </div>
      </div>
      <div class="other-service">
        <h2>その他のサービス</h2>
        <div class="service-detail">
          <p>裁判関連業務</p>
          <p>供託手続</p>
          <p>帰化申請</p>
          <p>相続遺言</p>
          <p>公正証書作成</p>
          <p>法律相談</p>
        </div>
      </div>
    </div>
    <!------------------
     -----Features------
     ------------------>
    <div clas="feature mg-80">
      <h1 class="section-ttl">事務所の特徴</h1>
      <div class="feature-wrap" >
        <div class="feature-card" v-for="(data,index) in feature" :key="index">
          <div class="feature-card-ttl">
            <img class="feature-icon" :src="data.icon" alt="" />
            <h2>{{data.ttl}}</h2>
          </div>
          <div class="feature-detail">
            <p class="feture-card-content">
              {{data.content}}
            </p>
            <img class="feature-img" :src="data.img" alt />
          </div>
        </div>
      </div>
    </div>
    <!--------------
     -----News------
     -------------->
    <div class="news mg-80">
      <h1 class="section-ttl">お知らせ</h1>
      <div class="news-content">
        <div class="news1 flex">
          <p class="date">2021年02月23日</p>
          <p class="content"><a href="">駐車場のご案内</a></p>
        </div>
        <div class="news2 flex">
          <p class="date">2021年02月22日</p>
          <p class="content"><a href="">新しいホームページを公開致しました。</a></p>
        </div>
        <button class="news-button" @click="transition">> MORE</button>
      </div>
    </div>
    <!--------------
     -----Access------
     -------------->
    <div class="access mg-80">
      <h1 class="section-ttl">アクセス</h1>
      <div class="access-info"> 
        <div class="left">
          <img src="../assets/company-logo.png" alt="company-logo" />
          <p class="address">〒567-0824<br> 大阪府茨木市中津町21番18号<br>ジュネス茨木ビル１階</p>
          <span>TEL</span><p class="tel">072-637-5141</p>
          <span>営業時間</span><p class="open-hours">平日：9:00～18:00<br>土日祝日：予約にて対応致しております。</p>
        </div>
        <div class="right">
          <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1637.821541163494!2d135.58173505792846!3d34.81492039510136!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6000e2bf4b146839%3A0x47db4d50c46e01db!2z44CSNTY3LTA4MjQg5aSn6Ziq5bqc6Iyo5pyo5biC5Lit5rSl55S677yS77yR4oiS77yR77yY!5e0!3m2!1sja!2sjp!4v1613969955866!5m2!1sja!2sjp" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      service: [
        {
          img:require("../assets/house.jpeg"),
          alt:"不動産登記",
          ttl:"不動産登記",
          description: "不動産に関する登記・会社法人に関する登記などを承っております。"
        },
        {
          img:require("../assets/elders.jpeg"),
          alt: "成年後見人",
          ttl:"成年後見人",
          description: "安心した生活を送れるよう司法書士がサポート致します。"
        },
        {
          img:require("../assets/money.jpeg"),
          alt: "債務整理",
          ttl:"債務整理",
          description: "任意整理・過払金請求・自己破産・民事再生などの手続きを行います。"
        }
      ],
      feature: [
        {
          icon: require("../assets/feature-number1.png"),
          ttl:"親切丁寧な対応を心掛けております",
          content: "当司法書士事務所では、頼りになる男性司法書士と優しい女性司法書士が丁寧・親切にご対応致します。",
          img: require("../assets/feature1.jpeg"),
        },
        {
          icon: require("../assets/feature-number2.png"),
          ttl:"地域密着型を目指しております",
          content: "当事務所は大阪府茨木市に根差し、あらゆる悩みにお応えできるようご自宅やご希望の場所へ伺ってのご相談を承っております。",
          img: require("../assets/feature2.jpeg"),
        },
        {
          icon: require("../assets/feature-number3.png"),
          ttl:"土日祝日も対応致します（要予約制)",
          content: "平日は仕事などで忙しい方のため、土日祝日でもご相談を受け付けております。ご予約制となりますのでご連絡をお願い致します。",
          img: require("../assets/feature3.jpeg"),
        },
        {
          icon: require("../assets/feature-number4.png"),
          ttl:"様々なニーズにお応え致します",
          content: "お客様ごとにきちんとお時間をとり、丁寧でご納得頂けるご説明を心掛けておりますので安心してご相談下さい。",
          img: require("../assets/meeting-1184892_640.png"),
        }
      ]
    };
  },
  methods: {
    transition() {
      this.$router.push({name: ""});
    },
    link() {
      this.$router.push({name: "Service"});
    }
  }
}
</script>

<style scoped>
/* --------------
----Common----
-------------- */
.section-ttl {
  font-size: 1.5rem;
  text-align:center;
  border-bottom: 0.5px solid #333;
  padding: 25px 0;
  width: 80%;
  margin: 40px auto;
}
.mg-80 {
  margin-bottom: 80px;
}

/* --------------
----Firstview----
-------------- */

.eyecatch img {
  width: 80%;
  display: block;
  margin: 0px auto;
  margin-bottom: 50px;
}

/* --------------
-----Service-----
-------------- */

.service-wrap {
  width: 100%;
  display: flex;
  justify-content: center;
}
.service-card img {
  width: 100%;
  display: block;
}
.service-card{
  width: 25%;
  margin: 0 10px;
  text-align: center;
}
.service-card-ttl {
  font-size: 1.3rem;
  padding: 20px 0;
}
.service-card-content {
  line-height: 1.5rem;
  padding: 10px 0;
  width: 85%;
  margin: 0 auto;
}
.other-service h2 {
  font-size: 1.3rem;
  font-weight:bolder;
  text-align: center;
  padding: 50px 0;
}
.service-detail{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.service-detail p {
  margin:0 50px;
  width: 30%;
  border:1px solid #333;
  text-align: center;
  padding:15px;
  margin-bottom: 10px;
  font-size: 18px;
}

/* --------------
----Features-----
-------------- */

.feature-wrap {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.feature-card {
  width: 38%;
  margin: 15px;
} 
.feature-card-ttl {
  display: flex;
  align-items: center;
}
.feature-card-ttl h2 {
  font-size: 1.2rem;
  padding-left: 10px;
}
.feature-detail {
  display: flex;
  padding: 20px;
}
.feture-card-content {
  width: 65%;
  line-height: 30px;
  padding-top: 10px;
} 
.feature-img {
  width: 40%;
}

/* --------------
------News-------
-------------- */

.news-content {
  width: 60%;
  margin: 0px auto;
  padding-top: 50px;
}
.flex {
  display: flex
}
.news-content .date {
  padding-right: 20px;
  padding-bottom: 20px;
  margin-bottom: 20px;
  border-bottom: 1px solid #f7813d ;
  text-align: left;
}
.news-content .content {
  padding-left: 30px;
  font-size: 1.3rem;
}
.content a {
  text-decoration: none;
  cursor: pointer;
}
.content a:hover {
  opacity: 0.8;
}
.news-button {
  padding: 10px 25px;
  background-color: #FFA279;
  border: none;
  font-size: 14px;
  font-weight: bold;
  color: #fff;
  display: block;
  margin:0 0 0 auto;
  cursor: pointer;
  outline: none;
}
.news-button:hover {
  opacity: 0.8;
}

/* --------------
------Access-----
-------------- */


.access-info {
  display: flex;
  justify-content: center;
}
.left {
  width: 40%;
  font-size: 1.1rem;
}
.address {
  padding: 30px;
}
.left span {
  background-color:#FFA279;
  color: #fff;
  padding: 5px;
  margin-left:30px ;
  font-size: 15px;
}
.tel {
  padding:15px 30px;
}
.open-hours {
  padding:15px 30px;
  line-height: 1.6rem
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .mg-80 {
    margin-bottom: 35px;
  }
  .eyecatch img {
    width: 95%;
  }
  .section-ttl {
    font-size: 1.2rem;
    padding: 10px;
    margin: 25px auto;
  }
  .service-wrap {
    flex-wrap: wrap;
  }
  .service-card {
    width: 95%;
    margin: 0 auto;
    margin-bottom: 30px;
  }
  .service-card-content {
    width: 90%;
    font-size: 0.8rem;
    padding:0;
    font-weight: normal;
  }
  .service-card-ttl {
    font-size: 0.8rem;
    padding: 15px;
  }
  .service-detail p {
    font-size: 0.8rem;
    margin: 10px;
  }
  .service-wrap img {
    width: 60%;
    margin: 0 auto;
  }
  .other-service h2 {
    font-size: 1rem;
    padding: 20px;
  }
  .feature-card {
    width: 90%;
  }
  .feature-detail {
    display: block;
    padding-right: 0;
  }
  .feature-card-ttl h2 {
    font-size: 1rem;
  }
  .feature-card-ttl {
    justify-content: center;
  }
  .feture-card-content {
    width: 100%;
    font-size: 0.8rem;
    text-align: left;
    font-weight: normal;
  }
  .feature-img {
    width: 60%;
    display: block;
    margin: 0 auto;
  }
  .news1,
  .news2 {
    display: block;
    text-align: center;
  }
  .news-content {
    width: 100%;
    padding-top: 10px;
  }
  .news-content .content {
    font-size:0.8rem;
    text-align: center;
    margin: 0;
    padding: 0;
  }
  .news-content .date {
    font-size: 0.8rem;
    text-align: center;
    width: 35%;
    margin: 20px auto;
    padding: 0;
    padding-bottom: 8px;
  }
  .news-button {
    margin: 30px auto;
    padding: 5px 20px;
    font-size: 0.7rem;
  }
  .access-info {
    display: block;
    text-align: center;
  }
  .address {
  padding: 20px;
  }
  .left img {
    display: none;
  }
  .left {
    width: 100%;
    margin: 0 auto;
    font-size: 0.9rem;
  }
  .left span {
    margin: 0;
    font-size: 12px;
  }
  .map  {
    width: 95%;
    margin-top: 20px;
  }
}
</style>