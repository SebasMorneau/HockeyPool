<template>
  <v-container class="app-cards">
    <v-card elevation="9">
      <v-expansion-panels>
        <v-expansion-panel>
          <v-expansion-panel-header> Historique </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_H"
              :items="historique"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            13ᵉ édition - 2022
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2022"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            12ᵉ édition - 2021
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2021"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            11ᵉ édition - 2020
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2020"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            10ᵉ édition - 2019
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2019"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            9ᵉ édition - 2018
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2018"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            8ᵉ édition - 2017
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2017"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            7ᵉ édition - 2016
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2016"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            6ᵉ édition - 2015
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2015"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            5ᵉ édition - 2014
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers_G"
              :items="data2014"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            4ᵉ édition - 2013
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers"
              :items="data2013"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            3ᵉ édition - 2012
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers"
              :items="data2012"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            2ᵉ édition - 2011
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers"
              :items="data2011"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
          <v-expansion-panel-header>
            1ᵉʳᵉ édition - 2010
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <v-data-table
              class="elevation-1"
              :headers="headers"
              :items="data2010"
              :items-per-page="itemsPerPage"
              hide-default-footer
            ></v-data-table>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
  </v-container>
</template>

<script>
import pool2010 from "../data/pool_2010.json";
import pool2011 from "../data/pool_2011.json";
import pool2012 from "../data/pool_2012.json";
import pool2013 from "../data/pool_2013.json";
import pool2014 from "../data/pool_2014.json";
import pool2015 from "../data/pool_2015.json";
import pool2016 from "../data/pool_2016.json";
import pool2017 from "../data/pool_2017.json";
import pool2018 from "../data/pool_2018.json";
import pool2019 from "../data/pool_2019.json";
import pool2020 from "../data/pool_2020.json";
import pool2021 from "../data/pool_2021.json";
import pool2022 from "../data/pool_2022.json";
import historic_data from "../data/historic.json";

export default {
  name: "HelloWorld",

  data: () => ({
    itemsPerPage: 16,
    headers: [
      {
        text: "Rang",
        align: "start",
        value: "Rank",
      },
      { text: "Nom", value: "Name" },
      { text: "PJ", value: "PJ" },
      { text: "PTS", value: "PTS" },
      { text: "BTS", value: "BTS" },
      { text: "PAS", value: "PAS" },
      { text: "Ratio", value: "Ratio" },
      { text: "PUN", value: "PUN" },
      { text: "SAL", value: "SAL" },
      { text: "ECM", value: "ECM" },
      { text: "EC", value: "EC" },
    ],
    headers_G: [
      {
        text: "Rang",
        align: "start",
        value: "Rank",
      },
      { text: "Nom", value: "Name" },
      { text: "PJ", value: "PJ" },
      { text: "PTS", value: "PTS" },
      { text: "BTS", value: "BTS" },
      { text: "PAS", value: "PAS" },
      { text: "VIC", value: "VIC" },
      { text: "DP", value: "DP" },
      { text: "BL", value: "BL" },
      { text: "Ratio", value: "Ratio" },
      { text: "PUN", value: "PUN" },
      { text: "SAL", value: "SAL" },
      { text: "ECM", value: "ECM" },
      { text: "EC", value: "EC" },
    ],
    headers_H: [
      {
        text: "Nom",
        align: "start",
        value: "name",
      },
      { text: "1er", value: "1" },
      { text: "2e", value: "2" },
      { text: "3e", value: "3" },
      { text: "4e", value: "4" },
      { text: "5e", value: "5" },
      { text: "6e", value: "6" },
      { text: "7e", value: "7" },
      { text: "8e", value: "8" },
      { text: "9e", value: "9" },
      { text: "10e", value: "10" },
      { text: "11e", value: "11" },
      { text: "12e", value: "12" },
    ],
    data2010: pool2010,
    data2011: pool2011,
    data2012: pool2012,
    data2013: pool2013,
    data2014: pool2014,
    data2015: pool2015,
    data2016: pool2016,
    data2017: pool2017,
    data2018: pool2018,
    data2019: pool2019,
    data2020: pool2020,
    data2021: pool2021,
    pool2022: pool2022,
    historique: historic_data,
  }),
};
</script>


<style scoped>
.app-cards {
  padding-top: 40px;
}
</style>


