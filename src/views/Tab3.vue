<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Expenses</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-refresher slot="fixed" @ionRefresh="doRefresh($event)">
        <ion-refresher-content></ion-refresher-content>
      </ion-refresher>

      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Income</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-searchbar></ion-searchbar>

      <income v-for="item in items" :key="item.id" :item="item"></income>

      <ion-fab vertical="bottom" horizontal="end" slot="fixed">
        <ion-fab-button color="success">
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
      </ion-fab>

    </ion-content>
  </ion-page>
</template>

<script>
  import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent,IonSearchbar,IonRefresher,IonRefresherContent,IonFab,IonFabButton,IonIcon } from '@ionic/vue';
  import {add} from "ionicons/icons"
  import Income from "../components/income";

  export default  {
    name: 'Tab3',
    components: {
      Income,
     IonHeader, IonToolbar, IonTitle, IonContent, IonPage,IonSearchbar,IonRefresher,IonRefresherContent,IonFab,IonFabButton ,IonIcon},
    data(){
      return{
        items:[
          {
            id:1,
            description:"Payment for bolt ride home",
            amount:200,
            date:'2021-06-03'
          },
          {   id:2,
            description:"Payment for bolt ride home",
            amount:350,
            date:'06-06-2021'
          },
          {
            id:3,
            description:"Payment for bolt ride home",
            amount:125,
            date:'06-06-2021'
          },

        ]
      }
    },
    methods:{
      doRefresh(){
        console.log('refershed');
      }
    },
    setup(){
      return{
        add
      }
    }
  }
</script>