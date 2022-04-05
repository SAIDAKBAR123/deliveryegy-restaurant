<template>
<div>
    <v-card color="white" flat tile style="width: 100vw">
      <v-toolbar v-if="false" class="px-0 py-0 mx-0 elevation-0" flat>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title class="headline text-bold">Deliveryegy</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-toolbar>
      <v-row  class="mx-2 my-2" justify="space-between" align="center">
        <v-col cols="auto">
          <span class="display-1">Мои заказы</span>
        </v-col>
        <v-col cols="auto">
          <span
            ><svg
              width="14"
              height="15"
              viewBox="0 0 14 15"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M6 6.5V0.5H8V6.5H14V8.5H8V14.5H6V8.5H0V6.5H6Z"
                fill="black"
              />
            </svg>
          </span>
        </v-col>
      </v-row>
      <v-row justify="center" align="center" style="margin: 0.4px 0px">
        <v-col cols="12">
          <v-tabs
          background-color="transparent"
            v-model="tab"
            slider-color="green"
            fixed-tabs
            active-class="colorDone"
            class="tab_card"
          >
            <v-tab>
              <v-badge color="green" content="12"> Новый </v-badge>
            </v-tab>
            <v-tab>В процессе</v-tab>
            <v-tab>Готов</v-tab>
          </v-tabs>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mt-4" flat tile color="transparent">
      <v-tabs-items v-model="tab" background-color="transparent" >
            <v-tab-item style="background-color: #E5E5E5 !important">
              <New />
            </v-tab-item>
            <v-tab-item style="background-color: #E5E5E5 !important">
                <Process />
            </v-tab-item>
            <v-tab-item style="background-color: #E5E5E5 !important">
                <Finish />
            </v-tab-item>
          </v-tabs-items>
    </v-card>
  </div>
</template>

<script>
import Finish from './finishedOrder'
import New from './newOrder'
import Process from './processOrder'
export default {
  data () {
    return {
      tab: 0
    }
  },
  components: { Finish, New, Process }
}
</script>

<style lang="scss" scoped>
.tab_card {
  border-radius: 12px !important;
  height: 56px;
  background: #efeff4 !important;
  padding: 5px;
}
.v-tab {
  background: #efeff4 !important;
}
.v-tabs-slider {
  color: #efeff4 !important;
}
.colorDone {
  background: rgb(231, 241, 245) !important;
  border-bottom: none;
  border-radius: 3px solid green;
}
</style>
