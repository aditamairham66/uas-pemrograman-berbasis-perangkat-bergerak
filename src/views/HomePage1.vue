<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Aplikasi Panggilan Telepon</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Aplikasi Panggilan Telepon</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <p>
        <ion-item>
          <ion-label position="stacked">Nomor yang dihubungi : </ion-label>
          <ion-input type="number" v-model="phone"></ion-input>
        </ion-item>
      </p>

      <ion-button @click="dialCall()">Panggil</ion-button>

      <p>    
        NIM 	: 042409096
      </p>
      <p>
        Nama	: Muhammad Lucky Irham Aditama
      </p>
      <p>
        UPBJJ	: SEMARANG
      </p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonInput, IonItem, IonLabel, IonButton } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonInput,
    IonItem,
    IonLabel,
    IonButton
  },
  data() {
    return {
      phone: 0,
    }
  },
  methods: {
    dialCall() {
      window.open(`tel:${this.phone}`)
    },
  },
});
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
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
