<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Aplikasi Login</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Aplikasi Login</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <p>
        <ion-item>
          <ion-label position="stacked">Username: </ion-label>
          <ion-input type="text" v-model="username"></ion-input>
        </ion-item>
        <ion-item>
          <ion-label position="stacked">Password: </ion-label>
          <ion-input type="password" v-model="password"></ion-input>
        </ion-item>
      </p>

      <ion-button @click="Login()">Login</ion-button>

      <p>    
        Status 	: {{ status }}
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
      username: null,
      password: null,
      status: "Ditolak / Diterima",
    }
  },
  methods: {
    Login() {
      if (this.username == this.password) {
        this.status = 'Diterima'
      } else {
        this.status = 'Ditolak'
      }
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
