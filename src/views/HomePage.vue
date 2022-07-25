<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar
  }
});
</script>

<template>
  <ion-page>
    <!-- <ion-header :translucent="true">
      <ion-toolbar class="header">
        <ion-title>Translucent Blank</ion-title>
      </ion-toolbar>
    </ion-header> -->
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Fullscreen Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <img id="bg-img" src="assets/svg/login_bg.svg" alt="Background">
        <div id="right-container">
          <div class="right-col-container">
            <div class="right-item-one">
              <img src="assets/svg/abangka_icon.svg" alt="Abangka Icon"> 
              <div class="col-five">
                <p>bangka</p>
                <span>DMIN</span>
              </div>
            </div>
            <div class="right-item-two">
              Welcome back! Please enter your credentials.
            </div>
            <div class="right-item-three">
              <div class="right-item-three-input">
                <input type="text" placeholder="Enter Username">
                <img src="assets/svg/user.svg" alt="User Icon">
              </div>
              <div class="right-item-three-input">
                <input type="text" placeholder="Enter Password">
                <img src="assets/svg/pass.svg" alt="Lock Icon">
              </div>
              <div class="right-item-three-bottom">
                <a id="create-link">Create Account</a>
                <a id="forgot-link">Forgot Password?</a>
              </div>
            </div>
            <button class="login-btn">
              Login
            </button>
            <p class="footer">Powered by <strong>New Folder(4)</strong></p>
          </div>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<style scoped>

ion-content {
  --ion-background-color: white !important;
  --ion-text-color: #474A4F;
  position: relative;
}

.header {
  --background: white !important;
}

#container {
  text-align: center;
  height: 100vh;
  width: 100vw;
  position: absolute;
  left: 0;
  right: 0;
}

#bg-img {
  position: absolute;
  top:0;
  left: 0;
  height: 100%;
}

#right-container {
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 50%;
  height: 100%;
}
.right-col-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 50px;
}
/* right item one */
.right-item-one {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  gap: 5px;
}
.right-item-one img {
  width: 71px;
  height: 64px;
}
.col-five {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;

  /* border: 1px solid black; */
}
.col-five p {
  margin: 0;
  font-weight: bold;
  font-size: 20px;
  justify-items: flex-start;
}
.col-five span {
  margin: 0;
  font-weight: bold;
  font-size: 45px;
}

/* right item two */
.right-item-two {
  color: #676769;
  font-size: 14px;
}

/* login button */
.login-btn {
  height: 40px;
  width: 200px;
  border-radius: 15px;
  background: #FCCB01;

  color: #292525;
  font-size: 16px;
  font-weight: bold;
}
.login-btn:active {
  background: #FFFFFF;
  border: 2px solid #FCCB01;
  color: #FCCB01;
}
/* right-item-three */
.right-item-three {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 26px;
}

.right-item-three input {
  background: #FFFFFF;
  border-radius: 10px;
  border: 1px solid #a8a8a8;
  width: 354px;
  height: 40px;
  padding-left: 60px;
  padding-right: 20px;
  font-size: 14px;
  color: #676769;
}

.right-item-three input:active,
.right-item-three input:focus {
  outline: none;
  border: 2px solid #0BA0F2;
}
.right-item-three-input {
  background: #FFFFFF;
  border-radius: 10px;
  border: none;
  outline: none;
  width: 354px;
  height: 40px;
  position: relative;
}
.right-item-three-input img{
  position: absolute;
  top: 0;
  left: 0;
  padding-left: 20px;
  padding-top: 7px;
}

/* right-item-three-bottom */
.right-item-three-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 12px;
  width: 100%;
}
#create-link {
  font-weight: normal;
  color: #676769;
  text-decoration: underline;
  cursor: pointer;
}
#forgot-link {
  font-weight: 600;
  color: #0BA0F2;
  cursor: pointer;
}
/* footer */
.footer {
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  font-size: 14px;
  color: #474A4F;
  padding-bottom: 15px;
}
</style>
