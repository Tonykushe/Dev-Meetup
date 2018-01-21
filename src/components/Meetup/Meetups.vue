<template>
        <v-content>
                <v-container>
                        <v-layout row wrap >
                                <v-flex xs12 sm10 md8  offset-sm2>
                                        <v-card color="cyan darken-2" class="white--text">
                                                <v-container fluid grid-list-lg>
                                                        <v-layout row>
                                                                <v-flex xs5 sm4 md3>
                                                                        <v-card-media
                                                                        src="https://www.worldtravelguide.net/wp-content/uploads/2017/03/shu-Kenya-Nairobi-549814942-Sopotnicki-copy.jpg"
                                                                        height="125px" >
                                                                        </v-card-media>
                                                                </v-flex>
                                                                <v-flex>
                                                                        <v-card-title>
                                                                                 <div >
                                                                                         <div>  My Meetup </div> 
                                                                                         <div>Foster the People</div>
                                                                                </div>
                                                                        </v-card-title>
                                                                        <v-card-actions>
                                                                                <v-btn to="/meetups/:id">
                                                                                        <v-icon left>arrow_forward</v-icon>
                                                                                        View Meetup
                                                                                </v-btn>
                                                                        </v-card-actions>
                                                                </v-flex>
                                                        </v-layout>
                                                </v-container>
                                        </v-card>
                                </v-flex>
                        </v-layout>
                </v-container>
        </v-content>
  
</template>
<script>
export default {
  
}
</script>

<style scoped>

</style>


