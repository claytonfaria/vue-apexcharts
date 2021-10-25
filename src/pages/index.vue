<script setup lang="ts">
import type { ApexOptions } from 'apexcharts';
import Chart from 'vue3-apexcharts';

const options: ApexOptions = {
  chart: {
    id: 'vuechart-example',

  },
  xaxis: {
    categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998],

  },
}
const series = [{
  name: 'series-1',
  data: [30, 40, 45, 50, 49, 60, 70, 91],
}]

</script>

<template>
  <div class="bg-white flex justify-center text-gray-800 ">
    <Chart width="500" type="line" :options="options" :series="series"></Chart>
  </div>
  <div class="bg-white flex justify-center text-gray-800 ">
    <Chart width="500" type="bar" :options="options" :series="series"></Chart>
  </div>
  <div class="bg-white flex justify-center text-gray-800 ">
    <Chart width="500" type="area" :options="options" :series="series"></Chart>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
