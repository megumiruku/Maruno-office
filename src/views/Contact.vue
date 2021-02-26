<template>
  <div id="contact">
    <Header />
    <div class="ttl">
       <img src="../assets/CONTACT.jpg" alt="お問い合わせ">
    </div>
    <div class="contact-info">
      <div class="tel">
        <h2 class="section-ttl">お電話でのお問い合わせ</h2>
        <div>
          <p class="number">TEL：072-637-5141</p>
          <p class="hours">受付時間 平日：9:00～18:00</p>
        </div>
      </div>
      <div class="form">
        <h2 class="section-ttl">メールでのお問い合わせ</h2>
      </div>
    </div>
    <form method="post" @submit.prevent="sendContact()">
      <div>
        <label for="name">お名前<span>必須</span></label>
        <input type="text" id="name" name="user_name"  v-model="name"/>
      </div>
      <div>
        <label for="name">フリガナ<span>必須</span></label>
        <input type="text" id="name" name="user_name" v-model="name2"/>
      </div>
      <div>
        <label for="mail">メールアドレス<span class="not-required">任意</span></label>
        <input type="email" id="mail" name="user_mail" v-model="email" />
      </div>
      <div>
        <label for="tel">お電話番号<span>必須</span></label>
        <input type="tel" id="tel" name="user_tel" v-model="tel" maxlength="15" />
      </div>
      <div>
        <label for="msg">ご相談内容<span>必須</span></label>
        <textarea id="msg" name="user_message" v-model="msg"></textarea>
      </div>
      <div class="button-submit">
        <button class="button" type="submit" >送信</button>
      </div>
    </form>
    <Footer />
  </div>
</template>

<script>
import Footer from '../components/Footer.vue'
import Header from '../components/Header.vue'
export default {
  data() {
    return {
      name: "",
      name2: "",
      email: "",
      tel: "",
      msg: "",
    }
  },
  methods: {
    sendContact() {
      if(
        this.name == "" ||
        this.name2 == "" ||
        this.tel == "" ||
        this.msg == "" 
      ){
        alert("入力されていない項目があります")
      }else {
        this.name = "";
        this.name2 = "";
        this.email = "";
        this.tel = "" ;
        this.msg = "" ;
        alert("送信しました")
      }
    }
  },
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
.contact-info{
  width: 70%;
  margin: 50px auto;
}
.section-ttl {
  margin: 20px 0;
  padding-left: 20px;
  border-left: 4px solid #f7813d;
  font-size: 1.4rem;
}
.tel div {
  background-color: #FFA279;
  width: 30%;
  padding:30px 50px;
  text-align: center;
  margin: 50px auto;
  font-weight: bold;
  border-radius: 3px;
}
.number{
  font-size: 1.5rem;
  padding-bottom: 10px;
  color: #fff;
}
.hours {
  font-size: 0.8rem;
  color: #fff;
}
form {
  width: 70%;
  margin: 70px auto;
  padding-left: 20px ;
  text-align: center;
}
span {
  margin-left: 20%;
  background-color: #FFA279;
  padding: 3px 8px;
  font-size: 14px;
  border-radius: 3px;
  color: #fff;
}
.not-required {
  background-color: rgb(160, 158, 158);
}
label {
  display:inline-block;
  width: 25%;
  text-align: left;
}
input,
textarea {
  box-sizing: border-box;
  border: 1px solid #999;
  width: 65%;
}
input {
  margin-bottom: 25px;
  padding: 7px;
}
textarea {
  vertical-align: top;
  height: 200px;
}
.button{
  width: 30%;
  margin:50px 0;
  text-align: center;
  padding: 10px 50px;
  font-size: 15px;
  background-color: #FFA279;
  color: #fff;
  border: none;
  border-radius: 3px;
  outline: none;
}
.button:hover {
  opacity: 0.8;
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .section-ttl {
    font-size: 1.1rem;
    margin-bottom: 30px;
  }
  .contact-info,
  form{
    width: 95%;
    margin-top: 30px;
    margin-bottom: 20px;
  }
  .tel div {
    width: 65%;
    margin: 40px auto;
    padding: 15px 20px;
  }
  .number{
    font-size: 1.2rem;
  }
  .hours {
    font-size: 0.8rem;
}
  label {
    display: block;
    margin: 10px auto;
    width: 80%;
    text-align: center;
    font-size: 1rem;
  }
  span {
    margin-left: 10px;
    font-size: 11px;
    margin-bottom: 10px;
  }
  input,
  textarea {
    width: 90%;
  }
  .button {
    width: 80%;
    margin-bottom: 20px;
  }
}
</style>