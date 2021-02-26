<template>
  <div id="footer">
    <div class="flex">
     <div class="left">
        <a href=""><img class="logo" src="../assets/company-logo_black.png" alt="company-logo" /></a>
      </div>
      <div class="right">
        <div class="nav">
          <ul class="header-nav flex">
            <li><a href="/">ホーム</a></li>
            <li><a href="/service">業務案内</a></li>
            <li><a href="/staff">スタッフ紹介</a></li>
            <li><a href="/about">事務所案内</a></li>
            <li><a href="/contact">お問い合わせ</a></li>
          </ul>
        </div>
      </div>
    </div>
    <small>Copyright (c) since 2010 Maruno Morimoto Shihoushoshi Jimusyo, All Rights Reserved.</small>
  </div>
</template>

<style scoped>
#footer {
  background-color: #FFAC77;
  text-align: center;
  opacity: 0.9;
}
.flex {
  display: flex;
  justify-content: center;
  text-align: center;
}
.left {
  width: 40%;
  margin-top: 15px;
}
.header-nav li {
  line-height: 100px;
  padding-right: 30px;
  list-style: none;
}
.header-nav a {
  text-decoration: none;
  cursor: pointer;
}
.header-nav a:hover {
  opacity: 0.7;
  border-bottom: 1px solid #333;
}
.logo {
  width: 70%;
}

@media screen and (max-width: 768px) {
  #footer {
    padding-bottom: 10px;
  }
  .flex {
    display: block;
  }
  .header-nav {
    display: none;
  }
  .left {
    display: block;
    width: 60%;
    margin: 0px auto;
    margin-top: 15px;
  }
  .logo {
    width: 95%;
    margin: 15px 0;
  }
  small {
    font-size: 10px
  }
}
</style>