<template>
    <div>
        <ion-card>
            <ion-item-sliding >
                <ion-item lines="none" type="full">
                    <ion-icon :icon="medkitOutline" slot="start"></ion-icon>
                    <ion-label style="padding: 10px">${{item.amount}} <br>
                        <small>{{item.description}}</small>
                    </ion-label>

                    <ion-label style="padding: 10px" slot="end">
                        <small>{{fromNow(item.date)}}</small>
                    </ion-label>
                </ion-item>
                <ion-item-options side="end" >
                    <ion-item-option @click="unread(item)" style="padding: 10px">View</ion-item-option>
                    <ion-item-option @click="unread(item)" style="padding: 10px">Edit</ion-item-option>
                    <ion-item-option color="danger" @click="unread(item)" style="padding: 10px">Delete</ion-item-option>
                </ion-item-options>
            </ion-item-sliding>
        </ion-card>

    </div>
</template>

<script>
    import {IonItemOptions,IonItemOption,IonIcon,IonCard,IonItemSliding,IonItem,IonLabel} from '@ionic/vue';
    import {medkitOutline}  from 'ionicons/icons';
    import moment from "moment";
    export default {
        props:['item'],
        name: "income",
        components:{IonItemOption,IonItemOptions,IonIcon,IonCard,IonItemSliding,IonItem,IonLabel},
        setup(){

            console.log(moment("20111031", "YYYYMMDD").fromNow());

            return{
                medkitOutline,


            }


        },
        methods:{
            fromNow(date){
                return moment(date, "YYYY-MM-DD").fromNow();

            }

        }
    }
</script>

<style scoped>
    .h-5{
        height: 70px;
    }


</style>