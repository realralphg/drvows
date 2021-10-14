<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <a href="/"><img src="logos/logo1240.png" style="height: 40px; max-width: 40px; padding-top: 5px;"></a>

        <q-toolbar-title class="text-h6">
          <router-link to="/" tag="span" style="cursor: pointer"> #DRvows </router-link>
        </q-toolbar-title>

        <q-space/>

        <q-btn no-caps flat class="gt-xs row" v-for="link in essentialLinks" :key="link.id" :to="link.to" exact clickable>
          <div class="column justify-center">
            <q-icon :name="link.icon" class="q-mr-xs" size="18px"/>
          </div>

          <div class="column q-mr-md">
            <q-item-label>{{link.label}}</q-item-label>
          </div>
        </q-btn>  

        <q-btn
          class="button"
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <q-footer>
      <div class="text-center bg-grey-10">
        <div class="text-primary">#DRvows</div>        
        <div class="text-grey-6">Copyright 2021</div>        
        <a href="https://www.wedvytes.com" target="_blank">wedvytes.com</a>
        <div class="text-grey-6">Greysoft Technologies</div>
      </div>
    </q-footer>

    <q-drawer
      v-model="leftDrawerOpen"
      :width="250"
      content-class="bg-primary"
    >
      <q-list>
        <q-item-label header class="text-white text-h5 text-weight-light">
          #DRvows
        </q-item-label>

        <q-item class="text-grey-5" v-for="link in essentialLinks" :key="link.id" :to="link.to" exact clickable>
          <q-item-section avatar>
            <q-icon :name="link.icon"></q-icon>
          </q-item-section>

          <q-item-section>
            <q-item-label>{{link.label}}</q-item-label>
          </q-item-section>
        </q-item>

      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',

  data () {
    return {
      leftDrawerOpen: false,

      essentialLinks: [
        {
          label: 'Home',
          icon: 'favorite',
          to: '/'
        },

        {
          label: 'Gift Registry',
          icon: 'favorite',
          to: '/giftregistry'
        },
      ]      
    }
  }
}
</script>

<style scoped>
@media (min-width: 600px){
  .button{
    display: none
  }
}

@media (max-width: 600px){
  #breadcrumbs{
    display: none
  }

.toolbar-title{
    display: none
  }
}

.q-router-link--exact-active{
  color: white !important;
}

.fixed-bottom{
  position:absolute;
}

a{
    text-decoration: none;
    color: rgb(233, 240, 239);        
}

</style>