    <script>
    import { Pie } from 'vue-chartjs';

    export default {
        extends: Pie,
        props: ['datachart', 'options'],
        mounted() {
            this.renderChart(this.datachart, this.options);
        },
    };
    </script>
