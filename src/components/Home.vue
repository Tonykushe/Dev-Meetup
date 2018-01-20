<template>
        <v-content>
                <v-container >
                        <v-layout row wrap>
                                <v-flex xs12 sm6 class="text-sm-right text-xs-center">
                                        <v-btn large  to="/meetups" class="error">Explore Meetups</v-btn>
                                </v-flex>
                                <v-flex xs12 sm6 class="text-sm-left text-xs-center">
                                        <v-btn large  to="/meetup/new" class="error">Organize Meetup</v-btn>
                                </v-flex>           
                        </v-layout>
                        <v-layout row wrap class="my-2">
                                <v-flex xs12>
                                        <v-carousel>
                                                <v-carousel-item 
                                                        v-for="meetup in meetups" 
                                                        :src="meetup.imageUrl"
                                                        :key="meetup.id">
                                                        <div class="title">
                                                                {{ meetup.title }}
                                                        </div>
                                                </v-carousel-item>
                                        </v-carousel>
                                </v-flex>
                        </v-layout>

                        <v-layout row wrap>
                                <v-flex xs12 class=" text-xs-center">
                                        <p>Join our awesome meetups!</p>
                                </v-flex>        
                        </v-layout>
                </v-container>
        </v-content>
</template>


<script>
export default {
        data() {
                return {
                        meetups: [
                                { imageUrl: 'https://www.worldtravelguide.net/wp-content/uploads/2017/03/shu-Kenya-Nairobi-549814942-Sopotnicki-copy.jpg', id: ' bfjabadkasdk ', title: ' Meetup in Nairobi ' },
                                { imageUrl: 'https://lonelyplanetimages.imgix.net/mastheads/GettyImages-538096543_medium.jpg?sharp=10&vib=20&w=1200', id: ' asdbsjbdjb ', title: ' Meetup in Newyork ' },
                                { imageUrl: 'http://www.telegraph.co.uk/content/dam/Travel/2016/August/Paris-travel-AP65117955-xlarge.jpg ', id: ' dadkaksdkj', title: ' Meetup in Paris ' },
                        ]
                }
        }
  
}
</script>

<style scoped>
.title {
        position: absolute;
        bottom: 50px;
        background-color: rgba(0, 0, 0, 0.5);
        color: white;
        font-size: 2em;
        padding: 20px;
}

</style>

