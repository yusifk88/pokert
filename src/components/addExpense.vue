<template>

    <div>

    <ion-fab vertical="bottom" horizontal="end" slot="fixed">
        <ion-fab-button>
            <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
    </ion-fab>
    </div>

</template>

<script>
    import {IonFab,IonFabButton,IonIcon } from '@ionic/vue';
    import {add} from "ionicons/icons";

    export default {

    name: "addExpense",
        components:{
        IonFabButton,
            IonFab,
            IonIcon
        },
        setup(){
        return{
            add
        }
        }
    }
</script>

<style scoped>

</style>