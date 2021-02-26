<template>
  <div id="header">
    <div class="flex">
      <div class="left">
        <a href=""><img class="logo" src="../assets/company-logo.png" alt="company-logo" /></a>
      </div>
      <div class="right">
        <div class="tel-info">
          <p class="tel-text">お気軽にお問い合わせください。</p>
          <span class="tel"><i class="fas fa-phone-alt icon-tel"></i>072-637-5141</span>
        </div>
        <button @click="transition"><i class="far fa-envelope icon-email"></i>お問い合わせ</button>
      </div>
    </div>
    <div class="nav">
        <ul class="header-nav">
          <li><a href="/">ホーム</a></li>
          <li><a href="/service">業務案内</a></li>
          <li><a href="/staff">スタッフ紹介</a></li>
          <li><a href="/about">事務所案内</a></li>
          <li><a href="/contact">お問い合わせ</a></li>
        </ul>
    </div>
    <div id="hamburger" @click="hamburger()" :class="{'active':isClass}">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="menu-content" :class="{'open':isClass}">
      <p class="menu-title">丸野・森本司法書士事務所</p>
      <ul class="menu_content_inner">
        <li><a href="/">ホーム</a></li>
        <li><a href="/service">業務案内</a></li>
        <li><a href="/staff">スタッフ紹介</a></li>
        <li><a href="/about">事務所案内</a></li>
        <li><a href="/contact">お問い合わせ</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClass: false
    };
  },
  methods: {
    transition() {
      this.$router.push({name: "Contact"});
    },
    hamburger() {
    this.isClass = !this.isClass;
    }
  }
};
</script>

<style scoped>
.flex {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
#header {
  width: 100%;
  padding:15px 0;
  margin: 0 auto;
  align-items: center;
}
.logo {
  width: 85%;
  margin-left: 170px;
  margin-top: 10px;
}
.right {
  width: 40%;
  display: flex;
  text-align: center;
}
.tel-info {
  margin: 25px;
  text-align: center;
}
.tel-text {
  font-size: 0.8rem;
  margin-bottom: 10px;
  padding-left: 20px;
  font-weight: bold;
}
.tel {
  font-size: 1.7rem;
  color:#f7813d;
}
.icon-tel {
  color: #f7813d;
  font-size: 25px;
  padding-right: 10px;
}
.right button {
  height: 60px;
  width: 150px;
  background:#FFA279;
  border: none;
  outline: none;
  margin:20px 20px;
  font-weight: bold;
  font-size: 1.1rem;
  color: #fff;
  border-radius: 10px;
  box-shadow: 5px 3px 3px rgba(0,0,0,0.3);
}
.right button:hover {
  opacity:0.7;
}
.icon-email {
  color: #fff;
  padding-right: 5px;
}
.nav {
  width: 90%;
  margin: 0 auto;
  height: 40px;
}
.header-nav {
  display: flex;
  justify-content: center;
  line-height: 40px;
  list-style: none;
}
.header-nav li {
  padding: 0 50px;
  border-right: 0.5px solid #333;
}
.header-nav >:nth-child(1) {
  border-left: 0.5px solid #333;
  padding-left: 50px;
}
.header-nav a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
  cursor: pointer;
  font-size: 1.2rem;
}
.header-nav a:hover {
  opacity: 0.7;
  border-bottom: 1px solid #333;
}
.menu-content {
  display: none;
}
@media screen and (max-width: 768px) {
  .right {
    display: none;
  }
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 20px;
    right: 20px;
    transition: 0.4s;
  }
  #hamburger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: #f7813d;
    transition: 0.8s;
  }
  #hamburger span:nth-of-type(1) {
    top: 10px;
  }
  #hamburger span:nth-of-type(2) {
    top: 20px;
  }
  #hamburger span:nth-of-type(3) {
    top: 30px;
  }
  .header-nav {
    display: none;
  }
  #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }
  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }
  .menu-content {
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: #fff;
    color: #333333;
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
    z-index: 999;
  }
  .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 1.2rem;
    color: #333333;
    text-align: left;
    font-weight: bold;
  }
  .menu-content li a {
    color: #333333;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid #FFA279;
    text-decoration: none;
    display: block;
  }
  .menu-content li {
    width: 100%;
    text-align: left;
  }
  .menu-content.open {
    left: 0;
  }
  #header {
    height: 50px;
    padding: 5px;
    margin-bottom: 20px;
  }
  .logo {
    margin-left: 5px;
    margin-top: 10px;
    width: 80%;
  }
}
</style>