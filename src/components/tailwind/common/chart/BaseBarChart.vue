<script>
    import {Bar} from 'vue-chartjs';
    import BaseChartMixin from '@/mixins/base-chart.mixin';

    export default {
        name: "BaseBarChart",
        extends: Bar,
        mixins: [
            BaseChartMixin
        ],
        mounted () {
            console.log('rendering');
            this.renderChart(this.chartData, this.chartOptions)
        },
        watch: {
            chartData: function(newVal) {
                this.renderChart(this.chartData, this.chartOptions)
            }
        }
    }
</script>