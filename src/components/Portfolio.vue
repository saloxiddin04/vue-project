<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium, numquam?</p>
      </v-col>
      <v-col lg="3" class="chip">
        <div class="text-center">
          <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp'? 'success': '' " class="mx-5">Web App</v-chip>
          <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp'? 'success': '' " class="mx-5">Mobile App</v-chip>
          <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio === 'desktopapp'? 'success': '' " class="mx-5">Desktop App</v-chip>
        </div>
      </v-col>
      <slot v-if="activePortfolio === 'webapp' ">
        <v-col lg="3" md="6" sm="12" v-for="(web,webindex) in webApps" :key="webindex">
          <v-card>
            <v-img :src="web.image" class="white--text" gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)">
              <v-card-title>{{web.title}}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio === 'mobileapp' ">
        <v-col lg="3" v-for="(mobile,mobileindex) in mobileApps" :key="mobileindex">
          <v-card>
            <v-img :src="mobile.image" class="white--text" gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)" height="200px">
              <v-card-title>{{mobile.title}}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio === 'desktopapp' ">
        <v-col lg="3" v-for="(desktop,desktopindex) in desktopApps" :key="desktopindex">
          <v-card>
            <v-img :src="desktop.image" class="white--text" gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)" height="200px">
              <v-card-title>{{desktop.title}}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: "PortfolioComponent",
    data(){
      return{
        activePortfolio: 'webapp',
        webApps:[
          {title: 'Web App 1', image:'https://images.pexels.com/photos/251225/pexels-photo-251225.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 2', image:'https://images.pexels.com/photos/1779487/pexels-photo-1779487.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 3', image:'https://images.pexels.com/photos/326503/pexels-photo-326503.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 4', image:'https://images.pexels.com/photos/699459/pexels-photo-699459.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 5', image:'https://images.pexels.com/photos/57690/pexels-photo-57690.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 6', image:'https://images.pexels.com/photos/669996/pexels-photo-669996.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Web App 7', image:'https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'}
        ],
        mobileApps:[
          {title: 'Mobile App 1', image:'https://images.pexels.com/photos/147413/twitter-facebook-together-exchange-of-information-147413.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 2', image:'https://images.pexels.com/photos/8970686/pexels-photo-8970686.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 3', image:'https://images.pexels.com/photos/8284723/pexels-photo-8284723.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 4', image:'https://images.pexels.com/photos/38544/imac-apple-mockup-app-38544.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 5', image:'https://images.pexels.com/photos/1092644/pexels-photo-1092644.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 6', image:'https://images.pexels.com/photos/1092671/pexels-photo-1092671.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'},
          {title: 'Mobile App 7', image:'https://images.pexels.com/photos/3912958/pexels-photo-3912958.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'}
        ],
        desktopApps:[
          {title: 'Desktop App 1', image:'https://avatars.mds.yandex.net/i?id=ac386a57576e9c84e9f8a9d6d185e926-4589723-images-thumbs&n=13'},
          {title: 'Desktop App 2', image:'https://i.pinimg.com/originals/1f/53/6b/1f536b464f01f7d7b9cf443e9edbbf77.jpg'},
          {title: 'Desktop App 3', image:'https://mir-s3-cdn-cf.behance.net/project_modules/1400_opt_1/529ec811358601.5a08ee3213d65.jpg'},
          {title: 'Desktop App 4', image:'https://www.digger.ru/storage/app/media/uploads/2015/02/Mac-redis-9.jpg'},
          {title: 'Desktop App 5', image:'https://i.pinimg.com/originals/81/47/98/8147986a0da0d6f1836a38ba41dcdfee.jpg'},
          {title: 'Desktop App 6', image:'https://myfreesoft.ru/wp-content/uploads/2019/11/computer-767781_1920.jpg'},
          {title: 'Desktop App 7', image:'https://boodet.online/wp-content/uploads/2021/04/2019-05-07-04-38-01-916-middle.jpeg'}
        ]
      }
    }
  }
</script>

<style scoped>
  @media only screen and (max-width: 768px) {
    .chip {
      flex-basis: auto;
    }
    .mx-5 {
      margin: 5px!important;
    }
  }
</style>