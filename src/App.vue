<template>
  <q-layout view="lHh Lpr lFf">
    <!-- <q-header elevated class="glossy">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
          icon="menu"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header> -->

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      class="bg-as-grey text-white side-bar"
      content-class="bg-as-grey"
      :width="260"
      :breakpoint="400"
    >
      <q-list>
        <q-item-label header>
          <img src="./assets/logo.svg"/>
        </q-item-label>
        <q-item-label header class="q-mb-lg text-white" style="opacity: 0.5;">
          Trusted way of banking for 3,000+ SMEs and startups in Singapore
        </q-item-label>
        
        <q-item clickable tag="a"  active-class="text-as-green">
          <q-item-section avatar>
            <img src="./assets/Home.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Home</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" to="/Cards" active-class="text-as-green">
          <q-item-section avatar>
            <img src="./assets/Card.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Cards</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a"  active-class="text-as-green">
          <q-item-section avatar>
            <img src="./assets/Payments.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Payments</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a"  active-class="text-as-green">
          <q-item-section avatar>
            <img src="./assets/Credit.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Credit</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a"  active-class="text-as-green">
          <q-item-section avatar>
            <img src="./assets/user.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Settings</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view></router-view>
    </q-page-container>
    <q-footer class="bottom-bar bg-white text-as-light-grey" elevated>
      <q-tabs  no-caps indicator-color="transparent">
        <q-route-tab to="" exact class="q-px-sm">
         <q-item-section align="center">
            <img src="./assets/Home-grey.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Home</q-item-label>
          </q-item-section>
        </q-route-tab>
        <q-route-tab to="/Cards" active-class="text-as-green" exact class="q-px-sm">
         <q-item-section align="center">
            <img src="./assets/Card.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Cards</q-item-label>
          </q-item-section>
        </q-route-tab>
        <q-route-tab to="" exact class="q-px-sm">
         <q-item-section align="center">
            <img src="./assets/Payments-grey.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Payments</q-item-label>
          </q-item-section>
        </q-route-tab>
        <q-route-tab to="" exact class="q-px-sm">
         <q-item-section align="center">
            <img src="./assets/Credit-grey.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Credit</q-item-label>
          </q-item-section>
        </q-route-tab>
        <q-route-tab to="" exact class="q-px-sm">
         <q-item-section align="center">
            <img src="./assets/user-grey.svg" style="height:20px"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Settings</q-item-label>
          </q-item-section>
        </q-route-tab>
      </q-tabs>
    </q-footer>
  </q-layout>
</template>

<script>



export default {
  name: 'LayoutDefault',

  components: {
    
  },

  data () {
    return {
      leftDrawerOpen: true
    }
  }
}
</script>
<style lang="scss">

$grey-color:#0C365A;
$blue-color:#325BAF;
$green-color:#01D167;
$light-grey:#DDDDDD;
$light-blue:#009DFF1A;
$light-green:#00D6B51A;
$light-red:#F251951A;




.text-as-green {
  color: $green-color !important;
}
.bg-as-green {
  background: $green-color !important;
}

.text-as-grey {
  color: $grey-color !important;
}
.bg-as-grey {
  background: $grey-color !important;
}

.text-as-blue {
  color: $blue-color !important;
}
.bg-as-blue {
  background: $blue-color !important;
}

.text-as-light-blue {
  color: $light-blue !important;
}
.bg-as-light-blue {
  background: $light-blue !important;
}

.text-as-light-green {
  color: $light-green !important;
}
.bg-as-light-green {
  background: $light-green !important;
}

.text-as-light-red {
  color: $light-red !important;
}
.bg-as-light-red {
  background: $light-red !important;
}

.text-as-light-grey {
  color: $light-grey !important;
}
.bg-as-light-grey {
  background: $light-grey !important;
}
.bottom-bar{
  display: none;
}
@media all and (max-width: 400px) and (min-width: 100px) {
	.bottom-bar{
    display: block;
  }
  .side-bar{
    display: none;
  }
}


</style>
