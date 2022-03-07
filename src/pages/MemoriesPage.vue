<!--creating a regular single file template component and connect it to a router - index.js-->

<template>
   <base-layout page-title="All Memories">
    <ion-list>
        <ion-list 
        v-for="memory in memories" 
        :router-link="`/memories/${memories.id}`"
        :key="memory.id">

        <ion-img :src="memory.image" :alt="memory.title"></ion-img>
        {{ memory.title }}
        </ion-list>
    </ion-list>
   </base-layout>
</template>

<script>
import { IonList, IonItem, IonImg } from '@ionic/vue';

export default {
    components: {
        IonList,
        IonItem,
        IonImg
    },
    data() {
        return {
            memories: [
                { 
                    id: 'm1',
                    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRRUN7LIddPb19PQq8EMoI8ZSw0ifwLuxWPKA&usqp=CAU',
                    title: 'A natural brocoli', 
                    description: 'What an amaizing natural creature!'
                },
                 { 
                    id: 'm2',
                    image: 'https://ichef.bbci.co.uk/news/976/cpsprodpb/6271/production/_114710252_pw_goldeneaglesproject-goldeneagle.jpg',
                    title: 'An eye for an eagles', 
                    description: 'I will always remember the good moment that we had!'
                },
                 { 
                    id: 'm3',
                    image: 'https://cdn.jwplayer.com/v2/media/lJbgbBfW/poster.jpg',
                    title: 'british most powerful dog', 
                    description: 'Do not come near!'
                },
                { 
                    id: 'm4',
                    image: 'https://everythingmountains.com/wp-content/uploads/2018/10/Traveling-By-Land-for-a-Trip.jpeg',
                    title: 'A trip to remember', 
                    description: 'Why do nations collide against each other at thie crucial moment!'
                },
            ],
        };
    }
};
</script>
<!--
<style scoped>
ion-title {
    background-color: linen;
}
ion-list {
    background-color: blue;
}
</style>
-->