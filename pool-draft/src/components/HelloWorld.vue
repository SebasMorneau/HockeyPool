<template>
  <v-container>
    <v-card elevation="9" shaped>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>11e édition - 2020</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>10e édition - 2019</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>9e édition - 2018</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>8e édition - 2017</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>7e édition - 2016</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>6e édition - 2015</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>5e édition - 2014</v-card-title>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>4e édition - 2013</v-card-title>
      <v-data-table
        class="elevation-1"
        :headers="headers"
        :items="data2013"
        :items-per-page="itemsPerPage"
        hide-default-footer
      ></v-data-table>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>3e édition - 2012</v-card-title>
      <v-data-table
        class="elevation-1"
        :headers="headers"
        :items="data2012"
        :items-per-page="itemsPerPage"
        hide-default-footer
      ></v-data-table>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>2e édition - 2011</v-card-title>
      <v-data-table
        class="elevation-1"
        :headers="headers"
        :items="data2011"
        :items-per-page="itemsPerPage"
        hide-default-footer
      ></v-data-table>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>1ère édition - 2010</v-card-title>
      <v-data-table
        class="elevation-1"
        :headers="headers"
        :items="data2010"
        :items-per-page="itemsPerPage"
        hide-default-footer
      ></v-data-table>
    </v-card>
  </v-container>
</template>

<script>
import pool2010 from "../data/pool_2010.json";
import pool2011 from "../data/pool_2011.json";
import pool2012 from "../data/pool_2012.json";
import pool2013 from "../data/pool_2013.json";

export default {
  name: "HelloWorld",

  data: () => ({
    itemsPerPage: 12,
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
    data2010: pool2010,
    data2011: pool2011,
    data2012: pool2012,
    data2013: pool2013,
  }),
};
</script>


<style scoped>
.mx-4 {
  padding-bottom: 50px;
}
.elevation-1 {
  padding: 20px;
}
</style>


