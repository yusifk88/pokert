<template>
  <ion-page>
    <ion-content :fullscreen="true" >

    <div class="blue-box">
      <ion-grid>
        <ion-row>
          <ion-col>
            <ion-icon class="large-icon text-light" :icon="searchOutline"></ion-icon>

          </ion-col>
          <ion-col style="text-align: right">
            <ion-icon class="large-icon text-light" :icon="menuOutline"></ion-icon>

          </ion-col>
        </ion-row>

        <ion-row>
          <ion-col>
            <h2 class="font-weight-light text-light" style="margin-top: 35px">Overview</h2>
          </ion-col>

        </ion-row>
      </ion-grid>

    </div>


      <ion-card style="margin-top: -140px; opacity: 0.9">
        <ion-card-header>
          <ion-card-subtitle>This Month</ion-card-subtitle>
          <ion-card-title>$200.00</ion-card-title>
        </ion-card-header>
        <ion-card-content>

          <main-line-chart></main-line-chart>
        </ion-card-content>
      </ion-card>

      <h6 class="ion-padding">RECENT EXPENSES</h6>
      <recent-expenses>

      </recent-expenses>

      <h6 class="ion-padding">RECENT INCOME</h6>

      <recent-income></recent-income>
    </ion-content>
  </ion-page>
</template>

<script >
import { IonIcon,IonPage, IonContent, IonGrid, IonRow,IonCol,IonCard,IonCardHeader,IonCardContent,IonCardTitle,IonCardSubtitle } from '@ionic/vue';
import { searchOutline,menuOutline} from 'ionicons/icons';
import MainLineChart from "@/views/charts/MainLineChart.vue";
import RecentExpenses from "@/components/recentExpenses";
import RecentIncome from "@/components/recentIncome";

export default  {
  name: 'Tab1',
  components: {
    RecentIncome,
    RecentExpenses,
    MainLineChart, IonContent, IonPage,IonGrid, IonRow,IonCol,IonIcon,IonCard,IonCardTitle,IonCardSubtitle,IonCardContent,IonCardHeader },
  setup(){

    return{
      searchOutline,
      menuOutline

    }
  }
}
</script>
<style scoped>

  .blue-box{
    background-color:#4270EF !important;
    padding: 10px;
    height: 300px;

  }

  .large-icon{
    font-size: 32px;
  }

  .font-weight-light{
    font-weight: normal;
  }

  .text-light{
    color: rgba(255, 255, 255, 0.83);

  }

</style>