<template>
  <q-page>
    <div class="full-width">
      <div class="row wrap q-gutter-md q-pr-md full-width bg-grey-2 q-py-md">
        <div class="col">
          <q-select
            outlined
            class="bg-white"
            label="Section name"
            dense
          ></q-select>
        </div>
        <div class="col">
          <q-select
            outlined
            class="bg-white"
            label="Subsection name"
            dense
          ></q-select>
        </div>
        <div class="col">
          <q-select
            outlined
            class="bg-white"
            label="Feeder name"
            dense
          ></q-select>
        </div>
        <div class="col">
          <q-select
            outlined
            class="bg-white"
            label="Date range"
            dense
          ></q-select>
        </div>
        <q-btn color="primary" label="Apply filters" no-caps></q-btn>
      </div>
      <div class="row">
        <div class="col-2 bg-grey-2 q-pt-md">
          <div style="height: 100%">
            <q-list>
              <q-item>
                <q-item-section>
                  <q-item-label>Single line item</q-item-label>
                  <q-item-label caption lines="2"
                    >Secondary line text. Lorem ipsum dolor sit amet,
                    consectetur adipiscit elit.</q-item-label
                  >
                </q-item-section>

                <q-item-section side top>
                  <q-item-label caption>5 min ago</q-item-label>
                  <q-icon name="star" color="yellow" />
                </q-item-section>
              </q-item>

              <q-separator spaced inset />

              <q-item>
                <q-item-section>
                  <q-item-label>Single line item</q-item-label>
                  <q-item-label caption
                    >Secondary line text. Lorem ipsum dolor sit amet,
                    consectetur adipiscit elit.</q-item-label
                  >
                </q-item-section>

                <q-item-section side top>
                  <q-item-label caption>Voted!</q-item-label>
                </q-item-section>
              </q-item>

              <q-separator spaced inset />

              <q-item>
                <q-item-section>
                  <q-item-label>Single line item</q-item-label>
                  <q-item-label caption
                    >Secondary line text. Lorem ipsum dolor sit amet,
                    consectetur adipiscit elit.</q-item-label
                  >
                </q-item-section>

                <q-item-section side top>
                  <q-badge color="teal" label="10k" />
                </q-item-section>
              </q-item>

              <q-separator spaced inset />

              <q-item>
                <q-item-section>
                  <q-item-label>Single line item</q-item-label>
                  <q-item-label caption
                    >Secondary line text. Lorem ipsum dolor sit amet,
                    consectetur adipiscit elit.</q-item-label
                  >
                </q-item-section>

                <q-item-section side top>
                  <q-item-label caption>2 min ago</q-item-label>
                  <div class="text-orange">
                    <q-icon name="star" />
                    <q-icon name="star" />
                    <q-icon name="star" />
                  </div>
                </q-item-section>
              </q-item>

              <q-separator spaced inset />

              <q-item>
                <q-item-section>
                  <q-item-label>Single line item</q-item-label>
                  <q-item-label caption
                    >Secondary line text. Lorem ipsum dolor sit amet,
                    consectetur adipiscit elit.</q-item-label
                  >
                </q-item-section>

                <q-item-section side top>
                  <q-item-label caption>meta</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </div>
        </div>
        <div class="col-7">
          <div class="row">
            <div class="col-12 q-pt-md q-px-md">
              <div class="chart-holder">
                <strong class="text-h5"
                  >Dow Jones Industrial Average (^DJI)</strong
                >
                <vue-apex-charts
                  width="100%"
                  height="400px"
                  :options="options"
                  :series="options.series"
                ></vue-apex-charts>
              </div>
            </div>
            <div class="full-width bg-grey-2 q-py-md"></div>
            <div class="col-6 q-pt-lg q-px-md">
              <strong class="text-h5">Current Month Performance</strong>
              <vue-apex-charts
                type="polarArea"
                width="100%"
                height="400px"
                :options="polarOptions.chartOptions"
                :series="polarOptions.series"
              ></vue-apex-charts>
            </div>
            <div class="col-6 q-pt-lg q-px-md">
              <strong class="text-h5">Meters Not Responded</strong>
              <vue-apex-charts
                type="bar"
                width="100%"
                height="400px"
                :options="barOptions.chartOptions"
                :series="barOptions.series"
              ></vue-apex-charts>
            </div>
          </div>
        </div>
        <div class="col-3">
          <div class="bg-grey-2 q-px-md" style="height: 100%">
            <q-card class="bg-white q-px-sm q-py-sm q-pb-md">
              <div class="row">
                <div
                  class="col-6 q-pb-md q-pt-md text-center border-right-bottom"
                >
                  <q-icon name="paid" color="secondary" size="30px"></q-icon>
                  <span class="block">Weekly Performance</span>
                  <strong class="block text-h5 text-bold text-primary"
                    >99.51%</strong
                  >
                  <p class="q-mb-none">
                    <q-icon
                      name="trending_up"
                      class="q-mr-xs"
                      color="green-14"
                    ></q-icon
                    ><b class="text-green-14">0.17%</b> vs last week
                  </p>
                </div>
                <div class="col-6 q-pb-md q-pt-md text-center border-bottom">
                  <q-icon name="euro" color="secondary" size="30px"></q-icon>
                  <span class="block">Meters Not Responded</span>
                  <strong class="block text-h5 text-bold text-primary"
                    >34.44%</strong
                  >
                  <p class="q-mb-none">
                    <q-icon
                      name="trending_down"
                      class="q-mr-xs"
                      color="red-10"
                    ></q-icon
                    ><b class="text-red-10">0.27%</b> vs last week
                  </p>
                </div>
                <div class="col-6 q-pb-md q-pt-md text-center border-right">
                  <q-icon
                    name="currency_yuan"
                    color="secondary"
                    size="30px"
                  ></q-icon>
                  <span class="block">8 hours SLA</span>
                  <strong class="block text-h5 text-bold text-primary"
                    >33.22%</strong
                  >
                  <p class="q-mb-none">
                    <q-icon
                      name="trending_up"
                      class="q-mr-xs"
                      color="green-14"
                    ></q-icon
                    ><b class="text-green-14">0.37%</b> vs last week
                  </p>
                </div>
                <div class="col-6 q-pb-md q-pt-md text-center">
                  <q-icon
                    name="currency_franc"
                    color="secondary"
                    size="30px"
                  ></q-icon>
                  <span class="block">12 hours SLA</span>
                  <strong class="block text-h5 text-bold text-primary"
                    >56.34%</strong
                  >
                  <p class="q-mb-none">
                    <q-icon
                      name="trending_up"
                      class="q-mr-xs"
                      color="green-14"
                    ></q-icon
                    ><b class="text-green-14">0.07%</b> vs last week
                  </p>
                </div>
              </div>
            </q-card>
            <q-card
              class="bg-white text-center q-mt-md q-px-sm q-py-sm q-pb-md"
            >
              <span class="text-h6">My portfolios</span>
              <p>Sign in to access your portfolio</p>
              <q-btn
                outline
                rounded
                color="accent"
                class="q-mr-sm"
                no-caps
                label="Sign in"
              />
            </q-card>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";

export default defineComponent({
  name: "IndexPage",
  components: {
    VueApexCharts,
  },
  data() {
    return {
      options: {
        series: [
          {
            data: [
              [1327359600000, 30.95],
              [1327446000000, 31.34],
              [1327532400000, 31.18],
              [1327618800000, 31.05],
              [1327878000000, 31.0],
              [1327964400000, 30.95],
              [1328050800000, 31.24],
              [1328137200000, 31.29],
              [1328223600000, 31.85],
              [1328482800000, 31.86],
              [1328569200000, 32.28],
              [1328655600000, 32.1],
              [1328742000000, 32.65],
              [1328828400000, 32.21],
              [1329087600000, 32.35],
              [1329174000000, 32.44],
              [1329260400000, 32.46],
              [1329346800000, 32.86],
              [1329433200000, 32.75],
              [1329778800000, 32.54],
              [1329865200000, 32.33],
              [1329951600000, 32.97],
              [1330038000000, 33.41],
              [1330297200000, 33.27],
              [1330383600000, 33.27],
              [1330470000000, 32.89],
              [1330556400000, 33.1],
              [1330642800000, 33.73],
              [1330902000000, 33.22],
              [1330988400000, 31.99],
              [1331074800000, 32.41],
              [1331161200000, 33.05],
              [1331247600000, 33.64],
              [1331506800000, 33.56],
              [1331593200000, 34.22],
              [1331679600000, 33.77],
              [1331766000000, 34.17],
              [1331852400000, 33.82],
              [1332111600000, 34.51],
              [1332198000000, 33.16],
              [1332284400000, 33.56],
              [1332370800000, 33.71],
              [1332457200000, 33.81],
              [1332712800000, 34.4],
              [1332799200000, 34.63],
              [1332885600000, 34.46],
              [1332972000000, 34.48],
              [1333058400000, 34.31],
              [1333317600000, 34.7],
              [1333404000000, 34.31],
              [1333490400000, 33.46],
              [1333576800000, 33.59],
              [1333922400000, 33.22],
              [1334008800000, 32.61],
              [1334095200000, 33.01],
              [1334181600000, 33.55],
              [1334268000000, 33.18],
              [1334527200000, 32.84],
              [1334613600000, 33.84],
              [1334700000000, 33.39],
              [1334786400000, 32.91],
              [1334872800000, 33.06],
              [1335132000000, 32.62],
              [1335218400000, 32.4],
              [1335304800000, 33.13],
              [1335391200000, 33.26],
              [1335477600000, 33.58],
              [1335736800000, 33.55],
              [1335823200000, 33.77],
              [1335909600000, 33.76],
              [1335996000000, 33.32],
              [1336082400000, 32.61],
              [1336341600000, 32.52],
              [1336428000000, 32.67],
              [1336514400000, 32.52],
              [1336600800000, 31.92],
              [1336687200000, 32.2],
              [1336946400000, 32.23],
              [1337032800000, 32.33],
              [1337119200000, 32.36],
              [1337205600000, 32.01],
              [1337292000000, 31.31],
              [1337551200000, 32.01],
              [1337637600000, 32.01],
              [1337724000000, 32.18],
              [1337810400000, 31.54],
              [1337896800000, 31.6],
              [1338242400000, 32.05],
              [1338328800000, 31.29],
              [1338415200000, 31.05],
              [1338501600000, 29.82],
              [1338760800000, 30.31],
              [1338847200000, 30.7],
              [1338933600000, 31.69],
              [1339020000000, 31.32],
              [1339106400000, 31.65],
              [1339365600000, 31.13],
              [1339452000000, 31.77],
              [1339538400000, 31.79],
              [1339624800000, 31.67],
              [1339711200000, 32.39],
              [1339970400000, 32.63],
              [1340056800000, 32.89],
              [1340143200000, 31.99],
              [1340229600000, 31.23],
              [1340316000000, 31.57],
              [1340575200000, 30.84],
              [1340661600000, 31.07],
              [1340748000000, 31.41],
              [1340834400000, 31.17],
              [1340920800000, 32.37],
              [1341180000000, 32.19],
              [1341266400000, 32.51],
              [1341439200000, 32.53],
              [1341525600000, 31.37],
              [1341784800000, 30.43],
              [1341871200000, 30.44],
              [1341957600000, 30.2],
              [1342044000000, 30.14],
              [1342130400000, 30.65],
              [1342389600000, 30.4],
              [1342476000000, 30.65],
              [1342562400000, 31.43],
              [1342648800000, 31.89],
              [1342735200000, 31.38],
              [1342994400000, 30.64],
              [1343080800000, 30.02],
              [1343167200000, 30.33],
              [1343253600000, 30.95],
              [1343340000000, 31.89],
              [1343599200000, 31.01],
              [1343685600000, 30.88],
              [1343772000000, 30.69],
              [1343858400000, 30.58],
              [1343944800000, 32.02],
              [1344204000000, 32.14],
              [1344290400000, 32.37],
              [1344376800000, 32.51],
              [1344463200000, 32.65],
              [1344549600000, 32.64],
              [1344808800000, 32.27],
              [1344895200000, 32.1],
              [1344981600000, 32.91],
              [1345068000000, 33.65],
              [1345154400000, 33.8],
              [1345413600000, 33.92],
              [1345500000000, 33.75],
              [1345586400000, 33.84],
              [1345672800000, 33.5],
              [1345759200000, 32.26],
              [1346018400000, 32.32],
              [1346104800000, 32.06],
              [1346191200000, 31.96],
              [1346277600000, 31.46],
              [1346364000000, 31.27],
              [1346709600000, 31.43],
              [1346796000000, 32.26],
              [1346882400000, 32.79],
              [1346968800000, 32.46],
              [1347228000000, 32.13],
              [1347314400000, 32.43],
              [1347400800000, 32.42],
              [1347487200000, 32.81],
              [1347573600000, 33.34],
              [1347832800000, 33.41],
              [1347919200000, 32.57],
              [1348005600000, 33.12],
              [1348092000000, 34.53],
              [1348178400000, 33.83],
              [1348437600000, 33.41],
              [1348524000000, 32.9],
              [1348610400000, 32.53],
              [1348696800000, 32.8],
              [1348783200000, 32.44],
              [1349042400000, 32.62],
              [1349128800000, 32.57],
              [1349215200000, 32.6],
              [1349301600000, 32.68],
              [1349388000000, 32.47],
              [1349647200000, 32.23],
              [1349733600000, 31.68],
              [1349820000000, 31.51],
              [1349906400000, 31.78],
              [1349992800000, 31.94],
              [1350252000000, 32.33],
              [1350338400000, 33.24],
              [1350424800000, 33.44],
              [1350511200000, 33.48],
              [1350597600000, 33.24],
              [1350856800000, 33.49],
              [1350943200000, 33.31],
              [1351029600000, 33.36],
              [1351116000000, 33.4],
              [1351202400000, 34.01],
              [1351638000000, 34.02],
              [1351724400000, 34.36],
              [1351810800000, 34.39],
              [1352070000000, 34.24],
              [1352156400000, 34.39],
              [1352242800000, 33.47],
              [1352329200000, 32.98],
              [1352415600000, 32.9],
              [1352674800000, 32.7],
              [1352761200000, 32.54],
              [1352847600000, 32.23],
              [1352934000000, 32.64],
              [1353020400000, 32.65],
              [1353279600000, 32.92],
              [1353366000000, 32.64],
              [1353452400000, 32.84],
              [1353625200000, 33.4],
              [1353884400000, 33.3],
              [1353970800000, 33.18],
              [1354057200000, 33.88],
              [1354143600000, 34.09],
              [1354230000000, 34.61],
              [1354489200000, 34.7],
              [1354575600000, 35.3],
              [1354662000000, 35.4],
              [1354748400000, 35.14],
              [1354834800000, 35.48],
              [1355094000000, 35.75],
              [1355180400000, 35.54],
              [1355266800000, 35.96],
              [1355353200000, 35.53],
              [1355439600000, 37.56],
              [1355698800000, 37.42],
              [1355785200000, 37.49],
              [1355871600000, 38.09],
              [1355958000000, 37.87],
              [1356044400000, 37.71],
              [1356303600000, 37.53],
              [1356476400000, 37.55],
              [1356562800000, 37.3],
              [1356649200000, 36.9],
              [1356908400000, 37.68],
              [1357081200000, 38.34],
              [1357167600000, 37.75],
              [1357254000000, 38.13],
              [1357513200000, 37.94],
              [1357599600000, 38.14],
              [1357686000000, 38.66],
              [1357772400000, 38.62],
              [1357858800000, 38.09],
              [1358118000000, 38.16],
              [1358204400000, 38.15],
              [1358290800000, 37.88],
              [1358377200000, 37.73],
              [1358463600000, 37.98],
              [1358809200000, 37.95],
              [1358895600000, 38.25],
              [1358982000000, 38.1],
              [1359068400000, 38.32],
              [1359327600000, 38.24],
              [1359414000000, 38.52],
              [1359500400000, 37.94],
              [1359586800000, 37.83],
              [1359673200000, 38.34],
              [1359932400000, 38.1],
              [1360018800000, 38.51],
              [1360105200000, 38.4],
              [1360191600000, 38.07],
              [1360278000000, 39.12],
              [1360537200000, 38.64],
              [1360623600000, 38.89],
              [1360710000000, 38.81],
              [1360796400000, 38.61],
              [1360882800000, 38.63],
              [1361228400000, 38.99],
              [1361314800000, 38.77],
              [1361401200000, 38.34],
              [1361487600000, 38.55],
              [1361746800000, 38.11],
              [1361833200000, 38.59],
              [1361919600000, 39.6],
            ],
          },
        ],
        chart: {
          id: "area-datetime",
          type: "area",
          height: 350,
          toolbar: {
            tools: {
              selection: false,
              reset: false,
              pan: false,
              zoom: false,
            },
          },
          zoom: {
            autoScaleYaxis: true,
          },
        },
        annotations: {
          yaxis: [
            {
              y: 30,
              borderColor: "#999",
              label: {
                show: true,
                text: "Support",
                style: {
                  color: "#fff",
                  background: "#00E396",
                },
              },
            },
          ],
          xaxis: [
            {
              x: new Date("14 Nov 2012").getTime(),
              borderColor: "#999",
              yAxisIndex: 0,
              label: {
                show: true,
                text: "Rally",
                style: {
                  color: "#fff",
                  background: "#775DD0",
                },
              },
            },
          ],
        },
        dataLabels: {
          enabled: false,
        },
        markers: {
          size: 0,
          style: "hollow",
        },
        xaxis: {
          type: "datetime",
          min: new Date("01 Mar 2012").getTime(),
          tickAmount: 6,
        },
        tooltip: {
          x: {
            format: "dd MMM yyyy",
          },
        },
        stroke: {
          width: 1,
          colors: ["#037b66"],
        },
        fill: {
          type: "gradient",
          colors: ["#037b66", "#FFFFFF"],
          gradient: {
            shadeIntensity: 1,

            opacityFrom: 0.7,
            opacityTo: 0.9,
            stops: [0, 100],
          },
        },
      },
      polarOptions: {
        series: [42, 47, 52, 58, 65],
        chartOptions: {
          chart: {
            width: 380,
            type: "polarArea",
          },
          labels: ["Item A", "Item B", "Item C", "Item D", "Item E"],
          fill: {
            opacity: 1,
          },
          stroke: {
            width: 1,
            colors: undefined,
          },
          yaxis: {
            show: false,
          },
          legend: {
            position: "bottom",
          },
          plotOptions: {
            polarArea: {
              rings: {
                strokeWidth: 0,
              },
              spokes: {
                strokeWidth: 0,
              },
            },
          },
          theme: {
            monochrome: {
              enabled: true,
              color: "#037b66",
              shadeTo: "light",
              shadeIntensity: 0.6,
            },
          },
        },
      },
      barOptions: {
        series: [
          {
            name: "Cash Flow",
            data: [
              1.45, 5.42, 5.9, -0.42, -12.6, -18.1, -18.2, -14.16, -11.1, -6.09,
              0.34, 3.88, 13.07, 5.8, 2, 7.37, 8.1, 13.57, 15.75, 17.1, 19.8,
              -27.03, -54.4, -47.2, -43.3, -18.6, -48.6, -41.1, -39.6, -37.6,
              -29.4, -21.4, -2.4,
            ],
          },
        ],
        chartOptions: {
          chart: {
            type: "bar",
            height: 350,
            toolbar: {
              tools: {
                selection: false,
                reset: false,
                pan: false,
                zoom: false,
              },
            },
          },
          plotOptions: {
            bar: {
              colors: {
                ranges: [
                  {
                    from: 0,
                    to: 10,
                    color: "#037b66",
                  },
                  {
                    from: 10,
                    to: 30,
                    color: "#ffd166",
                  },
                  {
                    from: -100,
                    to: -46,
                    color: "#037b66",
                  },
                  {
                    from: -45,
                    to: 0,
                    color: "#6de1c2",
                  },
                ],
              },
              columnWidth: "80%",
            },
          },
          dataLabels: {
            enabled: false,
          },
          yaxis: {
            title: {
              text: "Growth",
            },
            labels: {
              formatter: function (y) {
                return y.toFixed(0) + "%";
              },
            },
          },
          xaxis: {
            type: "datetime",
            categories: [
              "2011-01-01",
              "2011-02-01",
              "2011-03-01",
              "2011-04-01",
              "2011-05-01",
              "2011-06-01",
              "2011-07-01",
              "2011-08-01",
              "2011-09-01",
              "2011-10-01",
              "2011-11-01",
              "2011-12-01",
              "2012-01-01",
              "2012-02-01",
              "2012-03-01",
              "2012-04-01",
              "2012-05-01",
              "2012-06-01",
              "2012-07-01",
              "2012-08-01",
              "2012-09-01",
              "2012-10-01",
              "2012-11-01",
              "2012-12-01",
              "2013-01-01",
              "2013-02-01",
              "2013-03-01",
              "2013-04-01",
              "2013-05-01",
              "2013-06-01",
              "2013-07-01",
              "2013-08-01",
              "2013-09-01",
            ],
            labels: {
              rotate: -90,
            },
          },
        },
      },
    };
  },
});
</script>

<style lang="scss">
.border-bottom {
  border-bottom: dashed;
  border-color: #eee;
}
.border-right {
  border-right: dashed;
  border-color: #eee;
}
.border-right-bottom {
  border-bottom: dashed;
  border-right: dashed;
  border-color: #eee;
}
</style>
