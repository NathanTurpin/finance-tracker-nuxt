<template>
  <div>
    <section class="flex items-center justify-between mb-10">
      <h1 class="text-4xl font-extrabold">Summary</h1>
      <div>
        <USelectMenu v-model="viewSelected" :options="transactionViewOptions" />
      </div>
    </section>
    <section
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 sm:gap-16 mb-10"
    >
      <Trend
        color="green"
        title="Income"
        :amount="4000"
        :last-amount="3000"
        :loading="false"
      />
      <Trend
        color="red"
        title="Income"
        :amount="4000"
        :last-amount="5000"
        :loading="false"
      />
      <Trend
        color="green"
        title="Income"
        :amount="4000"
        :last-amount="3000"
        :loading="false"
      />
      <Trend
        color="red"
        title="Income"
        :amount="4000"
        :last-amount="5000"
        :loading="false"
      />
    </section>

    <section>
      <transcation />
      <transcation />
      <transcation />
      <transcation />
    </section>
  </div>
</template>

<script setup >
import { transactionViewOptions } from "../constants.js";
const viewSelected = ref(transactionViewOptions[0]);
</script>