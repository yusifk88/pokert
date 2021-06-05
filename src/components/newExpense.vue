<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>Add Expense</ion-title>
                <ion-buttons slot="end">
                    <ion-button>Close</ion-button>
                </ion-buttons>
            </ion-toolbar>

        </ion-header>

        <ion-content>
            <ion-header collapse="condense">
                <ion-toolbar>
                <ion-title>Add Expense</ion-title>
                </ion-toolbar>
            </ion-header>
            <ion-list class="ion-no-padding">

            <ion-item type="full" class="ion-padding-top">
                <ion-input class="p-input"  placeholder="Amount" ></ion-input>
            </ion-item>

            <ion-item type="full" class="ion-padding-top">
                <ion-input class="p-input"  placeholder="Category" ></ion-input>
            </ion-item>


            <ion-item type="full" class="ion-padding-top">
                <ion-input class="p-input"  placeholder="Payment Method" ></ion-input>
            </ion-item>



            <ion-item type="full" class="ion-padding-top">

                <ion-textarea
                    rows="2"
                    placeholder="Description"
                ></ion-textarea>

            </ion-item>



            </ion-list>

            <ion-button class="ion-margin" size="large" expand="block" color="primary" >Save</ion-button>

        </ion-content>


    </ion-page>

</template>

<script>
    import {IonPage,IonHeader,IonToolbar,IonTitle,IonButtons,IonButton,IonContent,IonInput,IonItem} from "@ionic/vue";
    export default {
        name: "newExpense",
        components:{IonPage,IonHeader,IonToolbar,IonTitle,IonButtons,IonButton,IonContent,IonInput,IonItem}
    }
</script>

<style scoped>
    ion-input{
        --background: rgba(128, 128, 128, 0.11);
        --padding-start:18px;
        --padding-top:18px;
        --padding-end:18px;
        --padding-bottom:18px;
        --border: 1px solid blue;
    }

    ion-textarea{
        --background: rgba(128, 128, 128, 0.11);
        --padding-start:18px;
        --padding-top:18px;
        --padding-end:18px;
        --padding-bottom:18px;
        --border: 1px solid blue;
    }


</style>