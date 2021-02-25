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
  height: 150px;
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
}
.header-nav li {
  padding-right: 30px;
  font-size: 17px;
  list-style: none;
  line-height: 130px;
}
.header-nav a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
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
    position: relative;
    height: 110px;
  }
  .flex {
    display: block;
  }
  .header-nav {
    display: none;
  }
  .left {
    width: 60%;
    margin: 0 auto;
  }
  .logo {
    width: 95%;
  }
  small {
    font-size: 10px;
    position: absolute;
    bottom: 25px;
    left: 5px;

  }
}
</style>