<template>
  <div class="cards">
    <v-container class="my-5">
      <v-layout class="card" row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="card in cards" :key="card.name">
          <v-card flat class="text-xs-center ma-3">
            <v-card-text class="text">
              <div class="border">
                <h1 class="subheading">
                  <!--<i class="fa fa-user right"></i>--><v-icon
                    class="right"
                    >{{ card.icon }}</v-icon
                  >
                  {{ card.name }}
                  <i class="fa fa-refresh left"></i>
                </h1>
              </div>
              <h2 class="role">{{ card.role }}</h2>
              <span class="percent">{{ card.percent }}</span>
            </v-card-text>
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
        {
          icon: "mdi-account-multiple",
          name: "العملاء الجدد",
          role: "0",
          percent: "(0%)",
        },
        {
          icon: "mdi-currency-usd",
          name: "مبيعات اليوم",
          role: "SAR 0",
          percent: "(0%)",
        },
        {
          icon: "mdi-chart-line",
          name: "ارباح اليوم",
          role: "SAR 0",
          percent: "(0%)",
        },
        {
          icon: "mdi-cash-fast",
          name: "فواتير اليوم",
          role: "0",
          percent: "(0%)",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.cards {
  margin-top: 250px;
  .v-sheet.v-card {
    margin: 10px;
    text-align: center;
    padding: 15px 0 30px 0;
    background: #272e48 !important;

    .border {
      background: #1d213b;
      padding: 10px;
      width: 100%;
      margin: 15px 0;
      border-radius: 5px;
      color: #eee;
      .subheading {
        color: #c4d2f0;
      }
      i {
        color: #5269ff;
        font-size: 25px;
      }
      .left {
        float: left;
      }
      .right {
        float: right;
      }
    }
    .subheading,
    .role {
      font-size: 21px !important;
      font-weight: bold !important;
    }
    .role {
      color: #808eaa;
      margin: 24px 0 10px 0;
    }
    .percent {
      color: #868ea4;
      font-weight: bold;
      font-size: 18px;
    }
    .v-card__subtitle,
    .v-card__text,
    .v-card__title {
      padding: 0 !important;
    }
  }
}
</style>
