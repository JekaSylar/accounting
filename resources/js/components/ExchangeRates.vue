<template>
  <div class="col s12 m6 l8">
    <div class="card orange darken-3 bill-card">
      <div class="card-content white-text">
        <div class="card-header">
          <span class="card-title">Курс валют</span>
        </div>
        <table v-if="courses">
          <thead>
            <tr>
              <th>Код валюты</th>
              <th>Курс покупки</th>
              <th>Курс продажи</th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="cours in courses" :key="cours.ccy">
              <td>{{ cours.ccy }}</td>
              <td>{{ cours.buy }}</td>
              <td>{{ cours.sale }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      courses: [],
    };
  },

  mounted() {
    this.LoaderCours();
  },

  methods: {
    LoaderCours() {
      axios
        .get(
          "https://api.privatbank.ua/p24api/pubinfo?exchange&json&coursid=11"
        )
        .then((res) => {
          this.courses = res.data;
        })
        .catch((err) => {
          console.warn("Ошибка с подключение к API банка ", error);
        });
    },
  },
};
</script>

<style >
.bill-card {
  height: 345px;
}
</style>
