<template>
    <div style="width: 80vw; height: 10vh; margin: 1.2rem auto">
        <canvas id="myChart"></canvas>
    </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'
import Chart from 'chart.js/auto'

// コンポーネントがマウントされたときにチャートを描画
onMounted(() => {
    const cnavas = document.getElementById('myChart') as HTMLCanvasElement

    //   都道府県名を修正できるかテストした部分
    const test: string = 'test'

    const ChartData = new Chart(cnavas, {
        type: 'line',
        data: {
            labels: ['A', 'B', 'C', 'D', 'E', 'F', 'G'],
            datasets: [
                {
                    label: '都道府県名',
                    data: [12, 19, 20, 4, 64, 0, 10],
                    backgroundColor: '#ffddcc',
                    borderColor: '#ff9966',
                    tension: 0.4
                },
                {
                    label: 'aaaa',
                    data: [120, 9, 200, 2111, 410, 21, 10],
                    backgroundColor: '#aaddcc',
                    borderColor: '#ffaa99',
                    tension: 0.4
                }
            ]
        },

        options: {
            responsive: true,
            scales: {
                x: {
                    display: true,
                    title: {
                        display: true,
                        text: '年代'
                    }
                },
                y: {
                    display: true,
                    title: {
                        display: true,
                        text: '人口構成'
                    }
                }
            }
        }
    })
    ChartData.data.datasets[0].label = test
    ChartData.update()
});
</script>
