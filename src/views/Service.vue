<template>
  <div id="service">
    <Header />
    <div class="ttl">
      <img src="../assets/SERVICE.jpg" alt="取り扱い業務">
    </div>
    <div class="explain">
      <h2 class="section-ttl">司法書士の役割とは？</h2>
      <div class="flex">
        <p class="explain-content">土地・家屋の権利に関する不動産登記や会社・法人に関する商業登記などの手続き、債務整理の相談等を申請人の代理にて行なう手続きと法律に関する専門家です。</p>
        <img src="../assets/feature1.jpeg" alt="司法書士のイメージ">
      </div>
    </div>
    <div class="service-all">
      <h2 class="section-ttl">取り扱い業務</h2>
      <div class="service-btns"> 
        <a href="#service1" class="btn">登記業務 </a>
        <a href="#service2" class="btn">成年後見 </a>
        <a href="#service3" class="btn">任意整理 </a>
        <a href="#service4" class="btn">自己破産 </a>
        <a href="#service5" class="btn">民事再生 </a>
        <a href="#service6" class="btn">その他 </a>
      </div>
    </div>
    <div class="service-detail">
      <div v-for="(data,index) in service" :key="index">
        <h3 :id="data.id" class="detail-ttl">{{data.ttl}}</h3>
        <div class="flex-2">
          <img :src="data.img" class="detail-img" :alt="data.alt" />
          <p class="detail-content">{{data.content}}</p>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header";
import Footer from "../components/Footer";
export default {
  data() {
    return {
      service: [
        {
          ttl:"登記業務",
          id: "service1",
          img: require("../assets/house.jpeg"),
          alt: "登記業務",
          content:"当事務所では、不動産の現況と権利関係を登記簿に記録して公示する不動産登記と会社・法人について、その存在を明確にするために一定事項を登記簿に記録して公示する商業・法人登記に関する登記業務を行っております。ご要望に応じて、これらの登記を行っておりますのでお気軽にお問い合わせください。"
        },
        {
          ttl: "成年後見",
          id: "service2",
          img: require("../assets/elders.jpeg"),
          alt: "成年後見",
          content: "認知症、知的障害、精神障害などが理由で、判断能力の不十分な方々は、財産を管理したり、介護サービス施設への入所に関する契約を結んだり、遺産分割の協議をしたりする必要があっても、自分でこれらのことをするのが難しい場合があります。また，契約などで不利益を被ってしまうおそれがあります。このような判断能力の不十分な方々を保護し、支援するのが成年後見制度です。　当事務所では、これらの手続きを行います。"
        },
        {
          ttl: "任意整理",
          id: "service3",
          img: require("../assets/money.jpeg"),
          alt: "任意整理",
          content: "裁判所などの公的機関を利用せずに、裁判外で金融業者と交渉を行い、利息・損害金・毎月の支払額の減免をしてもらい借金を整理する手続きの事。利息制限法に基づいて債務額を確定し債務者の収入の中から3年間（場合によっては5年程度）で返済します。"
        },
        {
          ttl: "自己破産",
          id: "service4",
          img: require("../assets/bankruptcy.jpg"),
          alt: "自己破産",
          content: "原則として破産の決定を受けた時点での自分の財産（生活に必要なものを除く）を失う代わりに、全ての債務が免除され、破産宣告以後の収入や新たに得た財産を債務の弁済に当てる事なく、経済的な更正を図るものです。"
        },
        {
          ttl: "民事再生",
          id: "service5",
          img: require("../assets/money.jpeg"),
          alt: "民事再生",
          content: "借金を圧縮し返済計画通りに返済を行います。破産の場合は財産を手放さなければなりませんが民事再生の場合は財産を守ることが可能です。住宅ローンをかかえている方、商売を続けたい方には最適な整理方法です。但し、自宅をのこす場合は、原則今まで通り住宅ローンは支払うことになり、その他の借金は圧縮されます。"
        },
        {
          ttl:"その他",
          id: "service6",
          img:require("../assets/money.jpeg"),
          alt: "その他",
          content: "裁判関連業務、供託手続、帰化申請、相続遺言、公正証書作成、法律相談なども行っております。"
        }
       
      ]
    }
  },
  components: {
    Header,
    Footer
  }
}
</script>

<style scoped>
.ttl {
  width: 100%;
  margin: 20px auto;
}
.ttl img {
  width: 100%;
}
.explain {
  width: 80%;
  margin: 70px auto;
}
.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
.section-ttl {
  margin: 20px 0;
  padding-left: 20px;
  border-left: 4px solid #f7813d;
  font-size: 1.8rem;
}
.explain-content {
  line-height: 2rem;
  width: 50%;
  margin-right:20px ;
  font-size: 1.5rem;
}
.explain img {
  width: 400px;
  display: inline-block;
  padding-bottom: 10px;
}
.service-all {
  width: 80%;
  margin: 20px auto;
  padding-bottom: 5%;
}
.service-btns {
  margin-top: 70px;
}
.service-all .btn {
  position: relative;
  border: 1px solid #333;
  display: inline-block;
  width: 240px;
  padding: 15px 18px;
  color: #333;
  font-size: 18px;
  text-align: left;
  text-decoration: none;
  margin:10px 25px;
  font-weight: bold;
  border-radius: 3px;

}
.btn::after {
  position: absolute;
  top: 40%;
  right: 25px;
  content: '';
  width: 8px;
  height: 8px;
  border-top: 2px solid #333;
  border-right: 2px solid #333;
  -webkit-transform: rotate(135deg);
  transform: rotate(135deg);
  transition: all .2s;
}
.btn:hover::after {
  opacity: 0.7;
  top: 45%;
}
.service-detail {
  width: 70%;
  margin: 0 auto;
  margin-bottom: 70px;
}
.detail-ttl {
  width: 30%;
  margin: 40px auto;
  font-size: 1.5rem;
  padding-bottom: 20px;
  border-bottom: 2px dashed #f7813d;
  text-align: center;
}
.flex-2 {
  display: flex;
  justify-content: center;
  align-items: center;
}
.detail-img {
  width: 40%;
  display: block;
}
.detail-content {
  margin-left: 5%;
  width: 50%;
  text-align: left;
  font-size: 1.1rem;
  line-height: 1.6rem;
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .ttl {
    margin: 30px 0;
  }
  .section-ttl {
    font-size: 1.1rem;
  }
  .explain,
  .service-all {
    margin-top: 30px;
    margin-bottom: 40px;
    width: 100%;
    /* background-color: blue; */
  }
  .explain-content {
    font-size: 0.9rem;
  }
   .flex {
    display: block;
    text-align:center;
  }
  .explain-content {
    width: 100%;
    margin: 0 auto;
    /* padding: 10px; */
    text-align: left;
  }
  .explain img{
    width: 80%;
  }
  .service-all .btn{
    margin: 5px;
    width: 200px;
  }
  .flex-2 {
    display: block;
    text-align: center;
  }
  .detail-ttl {
    width: 50%;
    font-size: 1rem;
    padding-bottom: 8px;
  }
  .detail-img {
    width: 90%;
    margin: 20px auto;
  }
  .detail-content {
    width: 100%;
    font-size: 0.8rem;
  }
}
</style>