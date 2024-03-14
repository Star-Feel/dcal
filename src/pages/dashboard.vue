<script setup lang="ts">
definePage({
  meta: {
    icon: 'mdi-monitor-dashboard',
    title: 'Dashboard',
    name:'出行/报警',
    drawerIndex: 1,
  },
})
const stats = ref([
  {
    icon: 'mdi-web',
    title: '越界报警',
    value: 230,
    unit: 'GB',
    color: 'primary',
    caption: 'Up: 100, Down: 130',
  },
  {
    icon: 'mdi-rss',
    title: '禁区报警',
    value: 108,
    color: 'primary',
    caption: 'Too young, too naive',
  },
  {
    icon: 'mdi-send',
    title: '明火报警',
    value: 1238,
    color: 'warning',
    caption: 'Limit: 1320',
  },
  {
    icon: 'mdi-bell',
    title: '密度报警',
    value: 9042,
    color: 'primary',
    caption: 'Warnings: 300, erros: 47',
  },
  // {
  //   icon: 'mdi-github',
  //   title: 'Github Stars',
  //   value: NaN,
  //   color: 'grey',
  //   caption: 'API has no response',
  // },
  // {
  //   icon: 'mdi-currency-cny',
  //   title: 'Total Fee',
  //   value: 2300,
  //   unit: '￥',
  //   color: 'error',
  //   caption: 'Upper Limit: 2000 ￥',
  // },
])
</script>

<template>
  <v-container fluid>
    <v-row>
      <v-col
        v-for="stat in stats"
        :key="stat.title"
        cols="12"
        sm="6"
        md="4"
        lg="2"
      >
        <StatsCard
          :title="stat.title"
          
          :color="stat.color"
          :icon="stat.icon"
          
        >
          <!--<template #footer>
            {{ stat.caption }}
          </template>-->
        </StatsCard>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6" lg="12">
        <v-card class="pa-2">
          <ChartLine />
        </v-card>
      </v-col>
      <!-- <v-col cols="12" md="6" lg="4">
        <v-card class="pa-2">
          <ChartRadar />
        </v-card>
      </v-col>
      <v-col cols="12" md="6" lg="4">
        <v-card class="pa-2">
          <ChartPie />
        </v-card>
      </v-col>
      <v-col cols="12" md="6" lg="4">
        <v-card class="pa-2">
          <ChartBar />
        </v-card>
      </v-col> -->
    </v-row>
    <video src="./../../public/20240222_192636.mp4" controls="true"  width="50%" height="50%"></video>
    <video src="./../../public/20240222_192636.mp4" controls="true"  width="50%" height="50%"></video>
    <video src="./../../public/20240222_192636.mp4" controls="true"  width="50%" height="50%"></video>
    <video src="./../../public/20240222_192636.mp4" controls="true"  width="50%" height="50%"></video>
  </v-container>
</template>

<style scoped>
.v-card:not(.stats-card) {
  height: 340px;
}
</style>
