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
        <img id="bg-img" src="assets/svg/login_bg.svg" alt="">
        <!-- <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p> -->
      </div>
    </ion-content>
  </ion-page>
</template>

<style scoped>

ion-content {
  --ion-background-color: white !important;
  position: relative;
}

.header {
  --background: white !important;
}

#container {
  text-align: center;
  height: 100vh;
  position: absolute;
  left: 0;
  right: 0;
  /* border: 1px solid red; */
}

#bg-img {
  position: absolute;
  top:0;
  left: 0;
  height: 100%;
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
