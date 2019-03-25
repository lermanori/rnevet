<template>
 <v-container>
    <v-container fluid  style="min-height:100px;">
    <transition v-if="shown"  name="page-transition" mode="out-in" appear enter-active-class="animated jackInTheBox"  leave-active-class="animated jackInTheBox">
      <h1 :class="this.$vuetify.breakpoint.xsOnly ? 'display-3 '+ styleStr: 'display-4 '+styleStr">
        algaeponix 
      </h1>
    </transition>
    </v-container>

    <v-container>
      <v-card>
    <v-parallax
    dark
    :src="require('../assets/lisanto.jpg')"
     >
    <v-layout
      align-center
      column
      justify-center
    >
      <h1 class="display-3 font-weight-thin my-3">Your Source For The World Of Algae</h1>
      
      <h4 class="headline font-weight-light mx-auto text-xs-center">
        Visit us to supply your healthy life! <br>
our nature pharmacy will change the health market. <br>
 ESEVFUND420 projects will supply all your body needs top down.
      </h4>
     
    </v-layout>
  </v-parallax>
      </v-card>
    </v-container>

    <v-container>
      <v-layout>
      <v-card class="mx-3">
        <v-card-title primary-title >
          <div>
            <h3 class="headline mb-0">Home</h3>
            <div> Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet, tempore. Dicta asperiores unde doloribus! Mollitia laborum inventore dolores beatae labore maiores doloribus blanditiis voluptatem. Suscipit ut vel accusantium optio, voluptas unde culpa quisquam eius iste, impedit vitae omnis quam, quae consequuntur debitis odio nisi? Nihil ut minima maxime modi optio labore? Molestiae exercitationem expedita totam et esse tempore nobis maxime fuga facere minima, laudantium laboriosam inventore, repellat, recusandae voluptate ipsum porro vel veritatis error sed consequuntur qui odio possimus quas! Perspiciatis numquam voluptatibus recusandae in ex, molestiae cupiditate libero, non totam tempore perferendis labore dicta sint id aliquam dolore aspernatur?</div>
          </div>
        </v-card-title>
      </v-card>
    </v-layout>
  </v-container>


    <v-container>
      <v-layout row wrap>
        <v-flex xs12 md6>
          
      <v-card class="ma-3">
        <v-img
          src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
          aspect-ratio="2.75"
        ></v-img>

        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
            <div> {{ card_text }} </div>
          </div>
        </v-card-title>

        <v-card-actions>
          <v-btn flat color="cyan">Share</v-btn>
          <v-btn flat color="cyan">Explore</v-btn>
        </v-card-actions>
      </v-card>
        

        </v-flex>
        
        <v-flex xs12 md6>
         
      <v-card class="ma-3">
        <v-img
          src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
          aspect-ratio="2.75"></v-img>

        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
            <div> {{ card_text }} </div>
          </div>
        </v-card-title>

        <v-card-actions>
          <v-btn flat color="cyan">Share</v-btn>
          <v-btn flat color="cyan">Explore</v-btn>
        </v-card-actions>
      </v-card>
         
        </v-flex>
        <app-cmplx-card/>

      </v-layout>
    </v-container>
 </v-container>
</template>

<script>
  import cmplxCard from '../components/cmplx-card'
  

  export default {
    data(){
      return {
        shown:false,
        styleStr:"text-truncate font-weight-thin mx-auto text-xs-center",
        card_text: "Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat."
              }
    },
    components:{
      'app-cmplx-card':cmplxCard
    }
    ,

    created(){
      setTimeout(() => {
        this.shown=true;
      }, 1000);
    }
  }
</script>
