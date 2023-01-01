<template>
  <div class="SkillChart" :id="contentId">
    <div class="ChartArea">
      <RadarChart
        :chart-id="contentId"
        :chart-data="chartData"
        :data="chartData"
        :size="{ width: 500, height: 400 }"
        :options="chartOptions"
        :margin="20"
      />
    </div>
    <!-- /.ChartArea -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Chart, ChartData, registerables } from "chart.js";
import { RadarChart } from "vue-chart-3";

Chart.register(...registerables);
export default defineComponent({
  name: "SkillChart",
  components: {
    RadarChart,
  },
  props: {
    contentId: {
      type: String,
      required: false,
    },
  },
  setup(props) {
    // Chart.defaults.font.family = "Lato";
    Chart.defaults.font.size = 16;
    // Chart.defaults.color = "#fff";
    // RadarChart 用のデータ
    const chartData: ChartData<"radar"> = {
      labels: [
        "文章・表作成",
        "コミュニケーション能力",
        "課題解決力",
        "マネジメント",
        "計画力",
      ],
      datasets: [
        {
          label: "自己評価",
          backgroundColor: "rgba(179,181,198,0.2)",
          //   backgroundColor: "#fff",
          borderCapStyle: "square",
          //線の色
          borderColor: "rgba(75, 192, 192,1)",
          //点の色
          pointBackgroundColor: "rgba(75, 192, 192,1)",
          //点の周りの色
          pointBorderColor: "#fff",
          //ホバー時の点の背景色
          pointHoverBackgroundColor: "#f5e107",
          //ホバー時の点の線の色
          pointHoverBorderColor: "#fff",
          //線の太さ
          borderWidth: 2,
          data: [5, 4.5, 3.5, 4, 4],
          //点の大きさ
          pointRadius: 6,
        },
      ],
    };
    const chartOptions = {
      responsive: true,
      maintainAspectRatio: true,
      scales: {
        r: {
          //グラフの最小値・最大値
          beginAtZero: true,
          min: 0,
          max: 5,
          stepSize: 1,
          //背景色
          backgroundColor: "snow",
          //グリッドライン
          grid: {
            color: "pink",
          },
          //アングルライン
          angleLines: {
            // display: false,
            color: "#faed58",
          },
          //各項目のラベル
          pointLabels: {
            color: "#fff",
            font: {
              size: 16,
            },
          },
        },
      },
    };
    return {
      chartData,
      chartOptions,
    };
  },
});
</script>

<style lang="scss" scoped></style>
