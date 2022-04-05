<template>
  <div>
    <v-card class="mb-2" color="white" style="border: 1px solid red" tile flat>
      <v-card-title class="text-h5 pa-2">
            <v-row justify="space-between" align="middle">
                <v-col cols="auto">
                    Заказ №134232
                </v-col>
                <v-col v-if="status !== 'newOrder'" cols="auto">
                    <v-chip color="red lighten-4">
                        <v-icon left color="red">mdi-clock-time-three-outline</v-icon>
                        <span class="red--text">09:21</span>
                    </v-chip>
                </v-col>
            </v-row>
        </v-card-title>
      <v-divider></v-divider>
      <v-card-subtitle class="pa-2 px-1">
        <v-row>
          <v-col cols="auto">
            <v-btn text small class="text-capitalize">
              <v-icon left size="24" color="green">mdi-bike</v-icon> Доставка
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-divider vertical></v-divider>
          </v-col>
          <v-col cols="auto">
            <v-btn text small>
              <v-icon left size="24" color="green">mdi-cash</v-icon> 160 000 сум
            </v-btn>
          </v-col>
        </v-row>
      </v-card-subtitle>
    </v-card>
  </div>
</template>

<script>
export default {
  props: ['status']
}
</script>

<style>
</style>
