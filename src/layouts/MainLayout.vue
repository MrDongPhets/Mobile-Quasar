<template>
  <q-layout view="lHh Lpr lFf">
    <q-header  style="background-color: white; z-index: 1; position: relative; width: 100%; 
    margin-bottom: 0; display: flex; flex-wrap: wrap;" >

      <q-toolbar class="flex justify-between ">
        <div class="flex justify-center" style="align-items: center;">
          <div>
            <q-icon name="supervised_user_circle" class="" style="font-size: 54px; color: #034f07;" />
          </div> 
         <div style="height: 50px;">
          <p style="font-size: 30px; margin: 0px; height: 35px; color: #005d6d;">CPA</p>
          <p style="font-size: 7px; margin: 0px; color: #005d6d;">Citizen Portal App</p>
         </div>

       
        </div>
       
        <div>
          <q-btn
          flat
          dense
          round
          icon="notifications"
          aria-label="Menu"
          style="color: #939393;"
        />

        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
           style="color: #939393;"
          @click="toggleLeftDrawer"
        />
        </div>
     

       
      </q-toolbar>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container style="padding: 1px;">
      <router-view />
    </q-page-container>

 
      <div style="width: 100%; padding: 5px; display: flex; justify-content: center; flex-wrap: wrap; gap: 30px;">
       <div style="width: 50px; height: 50px; display: flex; justify-content: center; flex-wrap: wrap;">
        <q-btn   flat  dense  round icon="person" class="" style="font-size: 20px;" @click="goToProfile" />
       <p style="margin-top: -10px;">Profile</p>
       </div>

       <div style="width: 50px; height: 50px; display: flex; justify-content: center; flex-wrap: wrap;">
        <q-btn flat  dense  round icon="mark_chat_unread" class="" style="font-size: 20px;" />
       <p style="margin-top: -10px;">Messages</p>
       </div>

       <div style="width: 50px; height: 50px; display: flex; justify-content: center; flex-wrap: wrap;">
        <q-btn flat  dense  round icon="home" class="" style="font-size: 20px;" @click="goToHome"/>
       <p style="margin-top: -10px;">Home</p>
       </div>

       <div style="width: 50px; height: 50px; display: flex; justify-content: center; flex-wrap: wrap;">
        <q-btn flat  dense  round icon="chat_bubble" class="" style="font-size: 20px;" />
       <p style="margin-top: -10px;">Messenger</p>
       </div>

       <div style="width: 50px; height: 50px; display: flex; justify-content: center; flex-wrap: wrap;">
        <q-btn flat  dense  round icon="history_edu" class="" style="font-size: 20px;" />
       <p style="margin-top: -10px;">Activity</p>
       </div>
      </div>
  
  </q-layout>
 
</template>

<script>
// import { ref } from 'vue'
// import EssentialLink from 'components/EssentialLink.vue'

// defineOptions({
//   name: 'MainLayout'
// })

// const linksList = [
//   {
//     title: 'Docs',
//     caption: 'quasar.dev',
//     icon: 'school',
//     link: 'https://quasar.dev'
//   },
//   {
//     title: 'Github',
//     caption: 'github.com/quasarframework',
//     icon: 'code',
//     link: 'https://github.com/quasarframework'
//   },
//   {
//     title: 'Discord Chat Channel',
//     caption: 'chat.quasar.dev',
//     icon: 'chat',
//     link: 'https://chat.quasar.dev'
//   },
//   {
//     title: 'Forum',
//     caption: 'forum.quasar.dev',
//     icon: 'record_voice_over',
//     link: 'https://forum.quasar.dev'
//   },
//   {
//     title: 'Twitter',
//     caption: '@quasarframework',
//     icon: 'rss_feed',
//     link: 'https://twitter.quasar.dev'
//   },
//   {
//     title: 'Facebook',
//     caption: '@QuasarFramework',
//     icon: 'public',
//     link: 'https://facebook.quasar.dev'
//   },
//   {
//     title: 'Quasar Awesome',
//     caption: 'Community Quasar projects',
//     icon: 'favorite',
//     link: 'https://awesome.quasar.dev'
//   }
// ]

// const leftDrawerOpen = ref(false)

// function toggleLeftDrawer () {
//   leftDrawerOpen.value = !leftDrawerOpen.value
// }

export default {
  data() {
    return {
      leftDrawerOpen: false
    };
  },
  methods: {
    goToProfile() {
      this.$router.push('/profile'); 
    },
    goToHome() {
      this.$router.push('/home');
    }
  }
}
</script>

<style scoped>
</style>