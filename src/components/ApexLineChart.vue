<template>

  <q-card class="chart-card">
      <!-- title and subtitle -->
      <q-card-section>
        <div class="text-h6">Total Value Locked</div>
        <div class="text-subtitle2">$100,000.00</div>
      </q-card-section>
      <!--/ title and subtitle -->

      <!-- badge 
      <div class="d-flex align-items-center flex-wrap mt-sm-0 mt-1">
        <h5 class="font-weight-bolder mb-0 mr-1">
          $ 100,000
        </h5>
        <b-badge variant="light-secondary">
          <feather-icon
            icon="ArrowDownIcon"
            size="16"
            class="text-danger mr-25"
          />
          <span class="align-middle">20%</span>
        </b-badge>
      </div>
      badge -->

<!-- chart -->
    <q-card-section>
      <vue-apex-charts
        type="line"
        height="400"
        :options="apexChatData.lineChartSimple.chartOptions"
        :series="apexChatData.lineChartSimple.series"
      />
    </q-card-section>
    <!--/ chart -->

  </q-card>
</template>

<script>
import VueApexCharts from 'vue-apexcharts'
import apexChatData from './apexChartData.js'

export default {
  components: {
    VueApexCharts
  },
  data() {
    return {
      apexChatData
    }
  },
}
</script>
