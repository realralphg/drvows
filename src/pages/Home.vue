<template>
    <div>
        <div>
          <div class="bg-grey-3">
            <div class="text-center">
                <img src="images/divider.png" alt="" width="80%" >
            </div>
            <div class="text-center">
                <span class="monsieur text-h3 text-weight-thin text-primary">Doosh & Ralph</span> <br>
                <span class="ruban text-h6 text-weight-light text-primary">#DRvows</span> <br>
                <span class="text-grey-7">We're getting married.</span>
            </div>
            <div class="text-center">
                <img src="images/divider.png" alt="" width="80%" >
            </div>   
          </div>
          <q-carousel
            v-model="slid"
            swipeable
            animated
            autoplay
            infinite
            control-color="secondary"
            :navigation="navigation"
            :navigation-position="navPos"
            height="400px"
            class="bg-grey-8 text-white"
            >

            <q-carousel-slide :name="carousel.name" class="q-pa-none" v-for="carousel in topCarousel" :key="carousel.id">
                <div>
                    <q-img :src="carousel.imageUrl" height="400px"/>
                    <div class="custom-caption absolute-bottom text-white text-h4 text-weight-light">
                    {{ carousel.title }}
                    </div>
                </div>
            </q-carousel-slide>
          </q-carousel>
        </div>

    <!-- Invitation C A R D -->
    <div class="row justify-center q-ma-md">
      <div class="text-center">
          <img src="images/divider.png" alt="" width="70%" >
      </div> 

      <q-card class="q-px-xl q-pt-xl text-white bg-secondary text-center" style="max-width: 350px">
        <span class="text-h4 text-weight-light text-warning align-center">Save The Date <br> </span>             
        <span class="text-h7 text-weight-light">WEDDING CEREMONY <br> </span>
        <span class="text-h7 text-weight-thin">6th November, 2021<br>Time: 10.00am <br> <br> </span>        
        <span class="text-h7 text-weight-thin">House on the Rock, Kaduna <br> Galaxy Multipurpose Hall <br>Janruwa Juction, Patrick Yakowa Express Way, Kaduna.<br> <br> </span>
        
        <span class="text-h7 text-weight-light">RECEPTION <br> </span>
        <span class="text-h7 text-weight-thin">Bouquet Hall - Ahmed Musa Neighbourhood Center <br> Patrick Yakowa Express Way, Kaduna.<br> <br> </span>

        <span class="text-h8">We are excited to celebrate with you! <br> </span> 
        <q-card-actions align="right">
          <a href="https://forms.gle/gaStXvZNsfFCzK8J9" target="_blank"><q-btn no-caps outline color="white" text-color="white" label="RSVP Now" /></a>
        </q-card-actions>          
      </q-card>      
    </div>

    <div class="text-center">
        <img src="images/divider.png" alt="" width="70%" >
    </div>  

      <div class="col-md-8 col-sm-8 col-xs-12">
        <div class="q-pa-md">
          <q-video
            :ratio="16/9"
            src="https://www.youtube.com/embed/XR6N4BJ3BMU"
          />
        </div>

        <div class="q-pa-md">
          <q-video
            :ratio="16/9"
            src="https://www.youtube.com/embed/u6NMEZtI5ek"
          />
        </div>
      </div>    

    <div class="text-center">
        <img src="images/divider.png" alt="" width="70%" >
    </div>  

    <div class="text-h5 text-weight-light text-primary text-center">Wedding Colors <br> </div>        
    <div class="text-center">
      <q-chip clickable color="primary" text-color="white">
        NavyBlue
      </q-chip>
      <q-chip clickable color="teal-10" text-color="white">
        EmeraldGreen
      </q-chip>
      <q-chip clickable color="amber-5" text-color="white">
        ChampagneGold
      </q-chip>            
    </div>

    <div class="text-center">
        <img src="images/divider.png" alt="" width="70%" >
    </div> 

    <!-- Couple Toast-->
    <!-- Two Cards - Groom-->
    <div class="row items-start justify-center  q-pa-md bg-grey-4 ">
      <q-card class="bg-primary" style="max-width: 300px">
          <img src="images/ralphh.jpg" alt="">
      </q-card>

      <q-card class="q-pa-md text-grey-7 bg-grey-3" style="max-width: 300px; width: 100%"> 
          <span class="text-weight-light text-h5 text-black">Lomla, baby</span>
          <p>Your beauty is more than can be visibly seen,
            for your mind is broad and your heart is full of love. 
            Your gentle spirit stills my raging sea
            and in your eyes are a thousand reasons to love and love again.<br>
            Darling, you're a blessing to me - my miracle! 
            Come thee yonder and rest in the confidence of my love for you.<br>
            From now till forever, in my bossom abide.</p>                
      </q-card>
    </div>

    <!-- Two Cards - Bride-->
    <div class="row items-start justify-center  q-pa-md bg-grey-4 ">
      <q-card class="q-pa-md text-grey-7 bg-grey-3" style="max-width: 300px; width: 100%"> 
          <span class="text-weight-light text-h5 text-black">Ralphy, love</span>
          <p>Loving you was worth the wait. I love you passionately.
            I love you intentionally. I love you today as I have from the start
            and I'll love you forever with all my heart.<br>
            Thank you for being my best friend. <br>
            Cheers to forever baby! </p>               
      </q-card>

      <q-card class="bg-primary" style="max-width: 300px">
          <img src="images/dooshh.jpg" alt="">
      </q-card>      
    </div> 

    <div class="bg-grey-8">
        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>          
        <div class="text-weight-light text-h4 text-white text-center">
          Our Love Story
        </div>
        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>
<!-- C H A T Love Story -->
        <div class="q-pr-md q-pl-md q-pb-md row justify-center">
            <div class="text-white" style="width: 100%; max-width: 500px">
              <q-chat-message
                label="Saturday, 19th"
              />

              <q-chat-message
                name="Dooshima"
                avatar="images/doosh.jpg"
                :text="['Story, story ooo... So in 2018 I attended a Youth meeting in HOTR, Kaduna and that was where I saw this dude. I liked him. ']"
                sent
                stamp="15 minutes ago"
              />
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['Only like?... mehnnn, she was crushing on me... lol. She is a beauty to behold but I thought she was a small geh so I just face front o!']"
                stamp="14 minutes ago"
              />
              <q-chat-message
                name="Dooshima"
                avatar="images/doosh.jpg"
                :text="['Lol... Well I fell in love with the monthly youth meetings, attended regurlarly and was soon recruited to join the Emerging Youth under the Tribe of Benjamin']"
                sent
                stamp="12 minutes ago"
              />
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['Yeah, funny thing, because not so long after she joined, the Tribe Head of Benjamin (Christine) was posted to Abuja (FCT) and as a rule, she was supposed to nominate a successor to lead in her stead - she nominated Dooshima!']"
                stamp="11 minutes ago"
              /> 
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['When she told me about her decision, I thought Dooshima was too young abi small to lead an entire tribe in the Emerging Youth Ministry BUT I WAS WRONG... Who would have thought she will be leading my life?']"
                stamp="9 minutes ago"
              /> 
              <q-chat-message
                name="Dooshima"
                avatar="images/doosh.jpg"
                :text="['You got that right... hehe. I accepted to lead the tribe and in his words, I did a pretty good job at it with his guidance... In those moments of showing me the ropes of leadership is where he truly got to know me and we began to connect!']"
                sent
                stamp="7 minutes ago"
              />     
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['This girl is intelligent. there is clearly more to her than meets the eye. We had long hours of communications, exhausting every topic... We talked about our problems and she particularly said she found peace and solution to her challenges whenever I counselled her.']"
                stamp="6 minutes ago"
              /> 
              <q-chat-message
                name="Dooshima"
                avatar="images/doosh.jpg"
                :text="['On the 23rd February, 2020. It was a Sunday evening... I received a text that read (I would love to see you). Booooommm! I knew this was meant to be something deep. He had never used the word LOVE in any sentence before now. He was always very careful with that word.']"
                sent
                stamp="5 minutes ago"
              /> 
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['After a warm hug... I went straight to the point, straighter than a ruler! I believe I am in love with you and would want us to date if that is okay with you...']"
                stamp="3 minutes ago"
              />  
              <q-chat-message
                name="Dooshima"
                avatar="images/doosh.jpg"
                :text="['What?! The joy was intense... Ralph is a good man. I have always liked him. I said yes and so we are here today, looking to share our vows come 6th November 2021. He says he is blessed to have me but I think I am more blessed... ']"
                sent
                stamp="2 minutes ago"
              />   
              <q-chat-message
                name="Ralph"
                avatar="images/ralph.jpg"
                :text="['...and this is only the beginning of our story! see you on the 6th of November... ']"
                stamp="1 minute ago"
              />                                                       
                                      
            </div>
          </div>                
    </div>

<!-- Pre-Wedding Photos -->
    <div class="bg-grey-8">
        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>

        <div class="text-weight-light text-h4 text-white text-center">
          Pre-wedding Photos
        </div>

        <div class="text-center q-mb-none q-pb-none">
          <img src="images/divider.png" alt="" width="80%" >
        </div>
<!-- Pictures Arrangements -->
        <div class="row q-mx-xl text-center"> 
<!-- Column One -->           
          <div class="col-xs-12 col-sm-6 col-md-6">

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic1.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic2.jpg" :ratio="4/3" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic14.jpg" :ratio="4/3" />
            </div> 

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic6.jpg" :ratio="4/3" />
            </div> 

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic15.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic16.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic17.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic22.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic23.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic24.jpg" :ratio="1" />
            </div>                                    
          </div>
<!-- Column Two -->
          <div class="col-xs-12 col-sm-6 col-md-6">
            <div class="q-pb-md">
                <q-img  class="radius" src="images/pic13.jpg" :ratio="4/3" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic26.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic10.jpg" :ratio="4/3" />
            </div>
            
            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic11.jpg" :ratio="4/3" />
            </div>  

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic18.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic30.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic20.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic21.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic29.jpg" :ratio="1" />
            </div>

            <div class="q-pb-md">
                <q-img class="radius"  src="images/pic25.jpg" :ratio="1" />
            </div>                        
          </div>                    
        </div>


        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>          
    </div>

<!-- Gift Registry -->
    <div class="bg-grey-4">
        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>          
        <div class="text-weight-light text-h4 text-grey-8 text-center">
          Gift Registry
        </div>
        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>

        <div class="text-grey-9 text-center q-mb-sm q-px-md">
          We are grateful in advance for all the pleasant gifts you have planned 
          to gift us with. You may wish to gift any of the items below or gift cash. 
          Again, thank you very plenty.
        </div>         
<!-- Gift Cards -->
        <div class="row justify-center q-gutter-md">
          <q-card class="bg-grey-3" style="width: 100%; max-width: 300px;">
            <img src="images/cash.jpg">
            <q-card-section>
              <div class="text-grey-8">
                Cash Gift
              </div>              
            </q-card-section>
            <q-card-actions align="right">
              <a href="https://paystack.com/pay/drvows" target="_blank"><q-btn no-caps glossy rounded color="primary" icon="favorite" label="Gift This" /></a>
            </q-card-actions>
          </q-card>

          <q-card class="bg-grey-3" style="width: 100%; max-width: 300px;">
            <img src="images/microwave.jpg">
            <q-card-section>
              <div class="text-grey-8">
                #50,000 - Hisense Microwave
              </div>              
            </q-card-section>
            <q-card-actions align="right">
              <a href="https://paystack.com/pay/drvows" target="_blank"><q-btn no-caps glossy rounded color="primary" icon="favorite" label="Gift This" /></a>
            </q-card-actions>
          </q-card>  

          <q-card class="bg-grey-3" style="width: 100%; max-width: 300px;">
            <img src="images/gascooker.png">
            <q-card-section>
              <div class="text-grey-8">
                #130,000 - Gascooker
              </div>              
            </q-card-section>
            <q-card-actions align="right">
              <a href="https://paystack.com/pay/drvows" target="_blank"><q-btn no-caps glossy rounded color="primary" icon="favorite" label="Gift This" /></a>
            </q-card-actions>
          </q-card>  

          <q-card class="bg-grey-3" style="width: 100%; max-width: 300px;">
            <img src="images/washing.jpg">
            <q-card-section>
              <div class="text-grey-8">
                #100,000 - Washing Machine
              </div>              
            </q-card-section>
            <q-card-actions align="right">
              <a href="https://paystack.com/pay/drvows" target="_blank"><q-btn no-caps glossy rounded color="primary" icon="favorite" label="Gift This" /></a>
            </q-card-actions>
          </q-card>                      
        </div>

<!-- Appreciation -->
        <div class="text-center q-pa-md">
          Thanks for your love <br>
          We are excited to celebrate with you! <br>  
          Watch this space for our post-wedding Photo Gallery!       
        </div>

        <div class="text-center">
          <img src="images/divider.png" alt="" width="80%" >
        </div>          

<!-- Floating Button -->
      <q-page-sticky position="bottom-right" :offset="[18, 18]">
        <q-fab
          v-model="fabRight"
          autoplay
          animated
          transition-prev="slide-right"
          transition-next="slide-left"    
          swipeable
          vertical-actions-align="right"
          color="primary"
          glossy
          icon="add"
          direction="up"
        >
          <q-fab-action label-position="left" color="primary" to="/giftregistry" icon="card_giftcard" label="Gift Registry" />
          <q-fab-action label-position="left" color="primary" @click="contactus=true" icon="phone" label="Contact Us" />
        </q-fab>  
      </q-page-sticky> 

    <!-- Dialogs -->
    <q-dialog v-model="contactus">
      <ContactUs/>
    </q-dialog> 

    </div>  
  </div>
</template>

<script>
import ContactUs from '../components/Dialogs/ContactUs'

export default {

    components:{
    ContactUs
  },

  data () {
    return {    
      fabRight: false,
      contactus: false,
    // for Carousel
      slid: 'moonlove',
      navigation: true,
      navPos: 'bottom',
      slide: 1,

      topCarousel: [
        {
          id: '1',
          name: 'moonlove',
          imageUrl: '/images/pic1.jpg',
          title: '6th November, 2021',
        },
        {
          id: '2',
          name: 'lovecircle',
          imageUrl: '/images/pic2.jpg',
          title: '#DRvows',
        },
        {
          id: '3',
          name: 'lovelove',
          imageUrl: '/images/pic3.jpg',
          title: '#Soulmates',
        },
        {
          id: '4',
          name: 'newlife',
          imageUrl: '/images/pic19.jpg',
          title: '#Newlife',
        },
        {
          id: '5',
          name: 'truelove',
          imageUrl: '/images/pic23.jpg',
          title: '#TrueLove',
        }, 
        {
          id: '6',
          name: 'marryme',
          imageUrl: '/images/pic28.jpg',
          title: '#MarryMe',
        },
        {
          id: '7',
          name: 'ring',
          imageUrl: '/images/pic27.jpg',
          title: '#Ring',
        },
        {
          id: '8',
          name: 'youandme',
          imageUrl: '/images/pic17.jpg',
          title: '#YouAndMe',
        },
        {
          id: '9',
          name: 'toserve',
          imageUrl: '/images/pic11.jpg',
          title: '#ToServe',
        },                                       
        {
          id: '10',
          name: 'loveRing',
          imageUrl: '/images/pic25.jpg',
          title: '#Forever',
        },                         
      ],      
    }
  }

}
</script>

<style scoped>

.custom-caption{
    bottom: 50px;
    text-align: center;
    padding: 12px;
    background-color: rgba(0, 0, 0, .3);
}

.radius{
  border-radius: 15px 0px 15px 0px;
  max-width: 350px;
}

.monsieur{
  font-family: 'Monsieur La Doulaise', 'Roboto', 'Arial';
}
.italiano{
  font-family: 'Italianno', 'Roboto', 'Arial';
}


/* .ruban{
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
} */
</style>
