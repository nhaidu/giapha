    <script>
    import { Doughnut } from 'vue-chartjs';

    export default {
        extends: Doughnut,
        props: ['dataDoughnut', 'optionsDoughnut'],
        mounted() {
            this.renderChart(this.dataDoughnut, this.optionsDoughnut);
        },
    };
    </script>
