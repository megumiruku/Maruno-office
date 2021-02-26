<template>
  <div id="staff">
    <Header />
    <div class="ttl">
      <img src="../assets/MEMBERS.jpg" alt="スタッフ紹介">
    </div>
    <div class="office">
      <h2 class="section-ttl">ごあいさつ</h2>
      <div class="flex">
        <p class="office-content">当丸野・森本司法書士事務所は、地元大阪府茨木市を中心とした、地元密着型司法書士事務所を目指しております。地域の皆様のお役に立てますよう、スタッフ一同、日夜努力しております。身近な町の法律家として、当事務所まで、お気軽にご相談下さい。</p>
        <img src="../assets/photo_staff.jpg" alt="スタッフ">
      </div>
    </div>
    <div class="profile">
      <h2 class="section-ttl">プロフィール</h2>
      <div class="profile-card flex">
        <div class="maruno">
            <h3 class="name">丸野 テル子</h3>
            <p class="description">法律事務所と税理士事務所勤務を経て、平成15年司法書士試験に合格。以後女性ならではのきめ細かなサービスと明るく元気をモットーに業務を行っております。</p>
            <ul>
              <li>大阪司法書士会会員</li>
              <li>簡裁訴訟代理等関係業務認定会員<br> （簡易訴訟代理認定番号：第312446号）</li>
              <li>(社)成年後見センター・リーガルサポート大阪支部会員</li>
            </ul>
        </div>
        <div class="morimoto">
            <h3 class="name">森本 理</h3>
            <p class="description">不動産会社を経て、平成5年司法書士試験合格、平成9年司法書士登録。仕事のモットーは、「地道にコツコツとガンバル」です。</p>
            <ul>
              <li>大阪司法書士会会員</li>
              <li>簡裁訴訟代理等関係業務認定会員<br> （簡易訴訟代理認定番号：第312446号）</li>
              <li>(社)成年後見センター・リーガルサポート大阪支部会員</li>
            </ul>
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
  components: {
    Header,
    Footer
  }
}
</script>

<style scoped>
.ttl {
  display: block;
  width: 80%;
  margin:20px auto;
}
.section-ttl {
  margin: 20px 0;
  padding-left: 20px;
  border-left: 4px solid #f7813d;
  font-size: 1.4rem;
}
.office {
  width: 80%;
  margin: 70px auto;
}
.flex {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.office-content {
  line-height: 1.8rem;
  width: 61%;
  margin-right: 20px ;
  font-size: 1.2rem;
}
.office img {
  display: inline-block;
  width: 30%;
  border-radius: 3px;
}
.profile {
  width: 80%;
  margin: 50px auto;
}
.name {
  text-align: center;
  font-size: 1.3rem;
  border-bottom: 3px dashed #f7813d;
  width: 25%;
  padding:10px;
  margin: 0 10px;
  margin-top: 20px;
}
.description {
  line-height: 1.5rem;
  padding: 20px;
  width: 90%;
}
.maruno,
.morimoto {
  width: 45%;
}
.profile li {
  list-style-position: inside;
  padding: 5px 0;
  line-height: 1.5rem;
  text-align: left;
  margin-left: 20px;
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .ttl{
    width: 100%;
    margin-bottom: 30px;
  }
  .section-ttl {
    font-size: 1rem;
  }
  .flex {
    display: block;
    align-items: center;
  }
  .office,
  .profile {
    width: 95%;
    margin-top:30px;
    margin-bottom: 35px;
  }
  .office-content {
    width: 95%;
    margin: 20px auto;
    line-height: 1.4rem;
    font-size: 0.8rem;
  }
  .office img {
    display: block;
    width: 70%;
    margin: 20px auto;
  }
  .maruno,
  .morimoto {
    width: 95%;
    margin: 20px auto;
    font-size: 0.8rem;
  }
  .name {
    font-size: 1rem;
    width: 50%;
    text-align: center;
    margin: 0px auto;
    margin-top: 20px;
  }
  .profile li {
    width: 95%;
    line-height: 1rem;
  }
}

</style>