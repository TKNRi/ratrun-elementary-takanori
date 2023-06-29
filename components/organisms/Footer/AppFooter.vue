<template>
  <footer class="footer">
    <div class="main">
      <div class="footer-contents">
        <div class="footer-left">
          <div class="footer-logo">
            <img src="../../../assets/png/logo-2.png" />
          </div>
          <div class="footer-left-p">
            <p>Interior design<br />&<br />Construction</p>
          </div>
        </div>
        <div class="footer-center1">
          <ul>
            <li>ホーム</li>
            <li>私達について</li>
            <li>選ばれる理由</li>
            <li>ワークフロー</li>
            <li>FAQ</li>
            <li>事例紹介</li>
          </ul>
        </div>
        <div class="footer-center2">
          <ul>
            <li>会社概要</li>
            <li>お問い合わせ・お見積</li>
            <li>個人情報保護法について</li>
          </ul>
        </div>
        <div class="footer-right">
          <div class="footer-text">
            <p>
              建築・建築デザイン・原状回復・内装解体・建築物解体・アスベスト除去工事はSENTIAにお任せください！
            </p>
            <div class="footer-text-about">
              <p>株式会社SENTIA</p>
              <p>454-0982</p>
              <p>愛知県名古屋市高見1-20-2</p>
              <p>TEL:052-1212-2029</p>
            </div>
          </div>
          <div class="footer-sns">
            <a></a>
            <a></a>
            <a></a>
          </div>
        </div>
      </div>
    </div>
  </footer>
  <div class="footer-copy">
    <p>Copyright © 店舗設計・デザイン・施工 CYPHER.AllRights Reserved</p>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scoped>
ul {
  list-style: none;
}
.footer {
  margin-top: 80px;
  background-color: gray;
  padding: 60px 60px;
  color: #fff;
}
.footer-contents {
  display: flex;
  justify-content: space-between;
  @include tablet {
    display: block;
    text-align: center;
  }

  @include mobile {
    display: block;
    text-align: center;
  }
}
.footer-left {
  text-align: center;
}
.footer-logo {
  margin-top: 20px;
}
.footer-center1 {
  li {
    padding: 10px 0;
  }
}
.footer-center2 {
  li {
    padding: 10px 0;
  }
}
.footer-right {
  width: 400px;
  @include tablet {
    width: 100%;
  }
  @include mobile {
    width: 100%;
  }
}
.footer-text {
  border: 8px double #fff;
  padding: 10px;
}
.footer-text-about {
  margin-top: 20px;
}
.footer-copy {
  text-align: center;
  padding: 20px 0;
}
</style>
