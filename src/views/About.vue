<template>
  <div id="about"> 
    <Header />
    <div class="ttl">
      <img src="../assets/ABOUT.jpg" alt="事務所案内">
    </div>
    <div class="about-office">
      <h2 class="section-ttl">事務所概要</h2>
      <div class="flex">
        <table  class="table">
          <tr>
            <th>事務所名</th>
            <td>丸野・森本司法書士事務所<p>簡裁訴訟代理認定番号 第312446号</p></td>
          </tr>
          <tr>
            <th>司法書士</th>
            <td>丸野 テル子・森本 理</td>
          </tr>
          <tr>
            <th>所在地</th>
            <td>〒567-0824 大阪府茨木市中津町21番18号 ジュネス茨木ビル１階</td>
          </tr>
          <tr>
            <th>営業時間</th>
            <td>平日：9:00～18:00<p>土曜・日曜・祝日：予約にて対応致しております</p></td>
          </tr>
          <tr>
            <th>連絡先</th>
            <td>TEL：072-637-5141<p>FAX：072-637-5143</p></td>
          </tr>
        </table>
        <div class="right">
          <img src="../assets/office-outside.jpg" alt="事務所外観" >
        </div>
      </div>
    </div>
    <div class="access">
      <h2 class="section-ttl">事務所アクセス</h2>
      <div class="flex">
        <div class="left">
          <div class="train">
            <h3 class="train-ttl">公共交通機関の場合</h3>
            <p class="train-access">阪急電車京都線「茨木駅」下車、東へ徒歩約10分です。</p>
          </div>
          <div class="car">
            <h3 class="car-ttl">お車の場合</h3>
            <p class="car-access">阪急電車京都線「茨木駅」を目指して頂き、更にその東側にあるジャスコ「新茨木店」を目標として頂くと分かりやすいと思います。</p>
          </div>
        </div>
        <div class="right">
          <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1637.821541163494!2d135.58173505792846!3d34.81492039510136!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6000e2bf4b146839%3A0x47db4d50c46e01db!2z44CSNTY3LTA4MjQg5aSn6Ziq5bqc6Iyo5pyo5biC5Lit5rSl55S677yS77yR4oiS77yR77yY!5e0!3m2!1sja!2sjp!4v1613969955866!5m2!1sja!2sjp" width="600" height="400" style="border:0;"  loading="lazy"></iframe>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '../components/Footer.vue';
import Header from '../components/Header.vue';

export default {
  components: { 
    Header, 
    Footer 
  },
}
</script>

<style scoped>
.ttl{
  display: block;
  width: 80%;
  margin: 20px auto;
}
.about-office {
  width: 80%;
  margin: 50px auto;
}
.flex {
  display: flex;
  align-items: center;
  justify-content: center;
}
.section-ttl {
  margin: 20px 0;
  padding-left: 20px;
  border-left: 4px solid #f7813d;
  font-size: 1.4rem;
}
.table {
  border: 1px solid #333;
  font-size: 0.9rem;
  width: 50%;
  margin-left: 30px;
}
.table td,
.table th {
  border: 1px solid #333;
  vertical-align: middle;
  padding:10px;
}
.right img {
  width: 75%;
  border-radius: 3px;
  margin-bottom: 25px;
}
.access {
  width: 80%;
  margin: 50px auto;
}
.flex {
  display: flex;
  justify-content: space-around;
}
.left {
  width: 70%;
  margin-right: 15px;
}
.train-ttl,
.car-ttl {
  padding:20px 0;
  font-size: 1.1rem;
  text-align: center;
}
.car-access,
.train-access {
  padding:10px 20px;
}
.right {
  padding-top:30px
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .ttl{
    width: 100%;
    margin-bottom: 30px;
  }
  .about-office,
  .access {
    width: 95%;
    margin-top: 30px;
    margin-bottom: 35px;
  }
  .section-ttl {
    font-size: 1rem;
    margin-bottom: 30px;
    padding-left: 15px;
    margin-left: 15px;
  }
  .flex {
    display: block;
  }
  .table {
    width: 85%;
    margin: 20px auto;
    border: none;
  }
  .table th { 
    border-bottom: none;
  }
  th, td {
    display: block;
    text-align: center;
  }
  .right img {
    width: 70%;
    display: block;
    margin: 0px auto;
    padding-bottom: 40px;
  }
  .left {
    width: 90%;
    margin: 10px auto;
    text-align: center;
  }
  .map {
    display: block;
    width:95%;
    margin: 20px auto;
  }
  .train-ttl,
  .car-ttl {
  padding:20px 0;
  font-size: 0.9rem;
  text-align: center;
  }
  .car-access,
  .train-access {
  font-size: 0.8rem;
  line-height: 1rem;
}
}
</style>
