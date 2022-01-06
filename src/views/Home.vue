<template>
  <v-app id="inspire" :style="{background: $vuetify.theme.themes.dark.background}">
    <SideBar />
    <SideBarRight />
    <v-container>
      <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n4">
        <v-btn-toggle v-model="toggle_exclusive" tile group color="#49D9A0">
          <v-btn text>
            <v-icon>fas fa-arrow-left</v-icon>
          </v-btn>
          <v-btn text>
            <v-icon>fas fa-arrow-right</v-icon>
          </v-btn>
        </v-btn-toggle>
        <v-spacer></v-spacer>
        <v-btn color="#49D9A0" rounded dark>
          finish sprint
        </v-btn>
      </v-toolbar>
      <v-item-group mandatory class="mt-n4">
        <v-container>
          <v-row justify="center" class="space">
            <v-col cols="12" md="2">
              <v-item v-slot="{active, toggle}">
                <v-card :color="active ? '#49D9A0' : 'white'" class="d-flex align-center rounded-xl" dark height="200" @click="toggle">
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="mt-10">
                        <v-list-item-content>
                          <div class="mb-4">
                            <v-icon x-large :color="active ? 'white' : '#49D9A0'">fas fa-chart-bar</v-icon>
                          </div>

                          
                          <v-list-item-subtitle :class="active ? 'white--text' : 'black--text'">Team velocity</v-list-item-subtitle>
                          <v-list-item-title class="headline mb-1" :class="active ? 'white--text' : 'black--text'"><strong>52</strong></v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
            <v-col cols="12" md="2">
              <v-item v-slot="{active, toggle}">
                <v-card :color="active ? '#49D9A0' : 'white'" class="d-flex align-center rounded-xl" dark height="200" @click="toggle">
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="mt-10">
                        <v-list-item-content>
                          <div class="mb-4">
                            <v-icon x-large :color="active ? 'white' : '#49D9A0'">fas fa-users</v-icon>
                          </div>

                          
                          <v-list-item-subtitle :class="active ? 'white--text' : 'black--text'">Team members</v-list-item-subtitle>
                          <v-list-item-title class="headline mb-1" :class="active ? 'white--text' : 'black--text'"><strong>12</strong></v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
            <v-col cols="12" md="2">
              <v-item v-slot="{active, toggle}">
                <v-card :color="active ? '#49D9A0' : 'white'" class="d-flex align-center rounded-xl" dark height="200" @click="toggle">
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="mt-10">
                        <v-list-item-content>
                          <div class="mb-4">
                            <v-icon x-large :color="active ? 'white' : '#49D9A0'">fas fa-suitcase</v-icon>
                          </div>

                          
                          <v-list-item-subtitle :class="active ? 'white--text' : 'black--text'">Tasks Delivered</v-list-item-subtitle>
                          <v-list-item-title class="headline mb-1" :class="active ? 'white--text' : 'black--text'"><strong>23</strong></v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
            <v-col cols="12" md="2">
              <v-item v-slot="{active, toggle}">
                <v-card :color="active ? '#49D9A0' : 'white'" class="d-flex align-center rounded-xl" dark height="200" @click="toggle">
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="mt-10">
                        <v-list-item-content>
                          <div class="mb-4">
                            <v-icon x-large :color="active ? 'white' : '#49D9A0'">fas fa-search</v-icon>
                          </div>

                          
                          <v-list-item-subtitle :class="active ? 'white--text' : 'black--text'">Spikes delivered</v-list-item-subtitle>
                          <v-list-item-title class="headline mb-1" :class="active ? 'white--text' : 'black--text'"><strong>23</strong></v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
            <v-col cols="12" md="2">
              <v-item v-slot="{active, toggle}">
                <v-card :color="active ? '#49D9A0' : 'white'" class="d-flex align-center rounded-xl" dark height="200" @click="toggle">
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="mt-10">
                        <v-list-item-content>
                          <div class="mb-4">
                            <v-icon x-large :color="active ? 'white' : '#49D9A0'">fas fa-globe-africa</v-icon>
                          </div>

                          
                          <v-list-item-subtitle :class="active ? 'white--text' : 'black--text'">News event</v-list-item-subtitle>
                          <v-list-item-title class="headline mb-1" :class="active ? 'white--text' : 'black--text'"><strong> 15</strong></v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
          </v-row>
        </v-container>
        
      </v-item-group>
    </v-container>
  </v-app>
</template>

<script>
import SideBar from '../components/SideBar'
import SideBarRight from '../components/SideBarRight'


import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { PieChart } from "echarts/charts";
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent,
} from "echarts/components";

use([
  CanvasRenderer,
  PieChart,
  TitleComponent,
  TooltipComponent,
  LegendComponent
]);


  export default {
    name: 'Home',

    data: () => ({
      toogle_exclusive: 1,
      orders: [
        {
          id: 'p42',
          title: 'Onboarding',
          state: 'Delivered',
          count: 3,
          icon: 'fas fa-ellipsis-h'
        },
        {
          id: 'p32',
          title: 'User Profile',
          state: 'Delivered',
          count: 8,
          icon: 'fas fa-ellipsis-h'
        },
        {
          id: 'p56',
          title: 'Landing Page',
          state: 'Approved',
          count: 12,
          icon: 'fas fa-ellipsis-h'
        },
        {
          id: 'p36',
          title: 'Settings',
          state: 'Approved',
          count: 9,
          icon: 'fas fa-ellipsis-h'
        },
      ],
      option: {
        title: {
          text: "Burnsown chart",
          left: "left",
        },
        tooltip: {
          trigger: "item",
          formatter: "{a} <br/>{b} : {c} ({d}%)"
        },
        series: [
          {
            name: "Traffic Sources",
            type: "pie",
            radius: "55%",
            center: ["45%", "50%"],
            data: [
              {value: 335, name: "Direct"},
              {value: 310, name: "Email"},
              {value: 234, name: "Ad Networks"},
              {value: 135, name: "Video ads"},
              {value: 1548, name: "Search Engines"},
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffset: 0,
                shadowColor: "rgba(0,0,0,0)"
              }
            }
          }
        ]
      }
    }),

    components: {
      SideBar,
      SideBarRight,
    },
    
  }
</script>

<style scoped>
  .space{
    margin-left: -100px;
    margin-right: -100px;
  }
</style>
