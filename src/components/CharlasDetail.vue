<template>
  <div>
    <div class="charlaDetailBox">
      <div class="charlaDetailImg">
        <div class="charlaDetailImg__box">
          <img src="https://imgur.com/veyASfn.png" width="115" height="115" alt />
        </div>
      </div>
      <div class="charlaDetailMeta">
        <div class="charlaDetailMeta__title">Pentesting con Python</div>
        <div class="charlaDetailMeta__author">Rafael Villarreal - 27/03/2018</div>
        <div class="charlaDetailMeta__tags">
          <div class="tag">python</div>
          <div class="tag">linux</div>
        </div>
      </div>
    </div>
    <div
      class="charlaDetailContent"
    >Muchas de las herramientas que se usan para pruebas de penetración en diferentes entornos están hechas con python. La idea es tomar alguna función pequeña de estas herramientas y recrearla con python.</div>
  </div>
</template>

<style>
.charlaDetailBox {
  margin: 5px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 850px;
  height: 140px;
  display: flex;
}

.charlaDetailContent {
  margin: 5px 5px 5px 130px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 595px;
  height: 140px;
  display: flex;
  font-size: 18px;
  letter-spacing: 0.05em;
  line-height: 22px;
}

.charlaDetailImg {
  width: 14%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaDetailImg__box {
  /* border-radius: 10px; */
  /* border: 0.5px solid #00a7e1; */
  height: 100px;
  width: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaDetailMeta {
  margin-top: 5px;
  margin-left: 15px;
}

.charlaDetailMeta__title {
  font-size: 36px;
}

.charlaDetailMeta__author {
  font-size: 18px;
  color: #4d646d;
}

.charlaDetailMeta__tags {
  display: flex;
  flex-direction: row;
}

.charlaDetailMeta__tags > .tag {
  margin-left: 5px;
}

.tag {
  background: #c4c4c4;
  box-sizing: border-box;
  border-radius: 4px;
  width: 70px;
  height: 20px;
  text-align: center;
  font-size: 14px;
}
</style>
