<template>
  <main class="home p-2">
    <div class="p-2">
      <h1 class="text-sky-900 font-bold">Dashboard</h1>
    </div>

<div class="cards">
 <div class="flex items-baseline mb-2">
      <div class="flex-none justify-center">
        <div class="mb-3 xl:w-40">
          <label for="floating_outlined" class="absolute text-sm duration-300 
          transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0
          peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">Weekly</label>
          <select
            name=""
            id="floating_outlined"
            class="form-select form-select-lg mb-3 appearance-none block w-full rounded m-0 bg-white bg-clip-padding bg-no-repeat border border-solid border-gray-300 text-gray-700 transition ease-in-out focus:text-gray-700 focus:bg-white focus:border-sky-600 focus:outline-none"
            aria-label=".form-select-lg"
          >
            <option selected>RTL WORLD</option>
            <option value="1">one </option>
            <option value="1">two</option>
            <option value="1">three</option>
            <option value="1">three</option>
          </select>
        </div>
      </div>

      <div class="flex-initial w-30">
        <div class="flex items-baseline mb-2 m-1">
          <div class="mb-3 xl:w-40">
          <select
            name=""
            id=""
            class="form-select form-select-lg mb-3 appearance-none block w-full rounded m-0 bg-white bg-clip-padding bg-no-repeat border border-solid border-gray-300 text-gray-700 transition ease-in-out focus:text-gray-700 focus:bg-white focus:border-sky-600 focus:outline-none"
            aria-label=".form-select-lg"
          >
            <option selected>Weekly</option>
            <option value="1">RTL WORLD</option>
            <option value="1">RTL WORLD</option>
            <option value="1">RTL WORLD</option>
            <option value="1">RTL WORLD</option>
          </select>
        </div>
        </div>
      </div>

    </div>

    <div class="grid grid-cols-4 mt-6">
      <DashboardCard title="Total revenue" priceOne="222,708" priceTwo="222,000" priceMin="708" icon="trending_up"/>
      <DashboardCard title="Total failed revenue" priceOne="35,079" priceTwo="34,000" priceMin="79" icon="trending_up"/>
      <DashboardCard title="Total failed revenue" priceOne="35,079" priceTwo="34,000" priceMin="79" icon="trending_up"/>
      <!-- <DashboardCard gradientBg="bg-gradient-to-r from-cyan-500 to-blue-500" title="Total failed revenue" priceOne="35,079" priceTwo="34,000" priceMin="79" icon="trending_up"/> -->

      <!-- <div
        class="shadow rounded-md p-2 m-2 bg-gradient-to-r from-cyan-500 to-blue-500"
      >
        3
      </div> -->
      <div class="shadow rounded-md bg-white p-2 m-2 bg-gradient-to-r">4</div>
    </div>
</div>

<div class="grid grid-cols-3 gap-4">
  <div class="bg-blue-300 rounded">06</div>
  <div class="col-span-2 bg-blue-700 rounded">07</div>
</div>

<div class="grid grid-cols-3 gap-4 mt-6">
  <div class="col-span-2 bg-blue-300">04</div>
  <div class="bg-blue-700">05</div>
</div>
   
  </main>
</template>

<script setup>
import DashboardCard from '../components/dashboard/DashboardCard.vue'
</script>
<style lang="scss" scoped>
.grid {
  @media (min-width: 768px) {
    flex-direction: column;
  }

  &h3 {
    color: #174c6f;
  }
}

.material-icons {
  background: #c5d5cb;
  color: #51b176;
  padding: 4px;
  border-radius: 4px;
}
</style>
