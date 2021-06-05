<template>
    <div>
     <expense v-for="item in items" :item="item" :key="item.id"></expense>
        <ion-button expand="full"><ion-icon :icon="add"></ion-icon> Expense </ion-button>
    </div>
</template>

<script>
    import Expense from "@/components/expense";
    import {IonIcon} from "@ionic/vue";
    import {add} from "ionicons/icons";
    export default {
        name: "recentExpenses",
        components: {Expense,IonIcon},
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
        setup(){
            return{
                add
            }
        }
    }
</script>

<style scoped>
    .h-5{
        height: 70px;
    }


</style>