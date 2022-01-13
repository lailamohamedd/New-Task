<template>
  <div class="card">
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="card in cards" :key="card.name">
          <v-card flat class="text-xs-center ma-3">
            <v-card-text>
              <div class="subheading">{{ card.name }}</div>
              <div class="grey--text">{{ card.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flex color="grey">
                <v-icon small left>reload</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        { name: "العملاء الجدد", role: "0", percent: "(0%)" },
        { name: "مبيعات اليوم", role: "SAR 0", percent: "(0%)" },
        { name: "ارباح اليوم", role: "SAR 0", percent: "(0%)" },
        { name: "فواتير اليوم", role: "0", percent: "(0%)" },
      ],
    };
  },
};
</script>
