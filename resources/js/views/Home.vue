<template>
  <div>
    <div class="page-title">
      <h3>Счет</h3>

      <button class="btn waves-effect waves-light btn-small">
        <i class="material-icons">refresh</i>
      </button>
    </div>

    <div class="row">
      <div class="col s12 m6 l4">
        <div class="card light-blue bill-card">
          <div class="card-content white-text">
            <span class="card-title">Счет в валюте</span>

            <p class="currency-line">
              <span>12.0 Р</span>
            </p>
          </div>
        </div>
      </div>

      <exchange-rates />
    </div>
  </div>
</template>

<script>
import ExchangeRates from "../components/ExchangeRates.vue";
export default {
  components: {
    ExchangeRates,
  },
};
</script>

<style>
</style>
