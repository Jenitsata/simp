<template>
  <div class="bg-yellow-50 w-screen h-screen">
    <div class="text-center p-10 px-50">
      <div class="row">
        <div
          class="flex flex-col text-base text-gray-700 md:text-lg text-center"
        >
          <h2 class="text-xl">ตะกร้าสินค้า</h2>
          <h3>
            สามารถซื้อสินค้าได้มากกว่า 1 เห็ดลม เงินในส่วนของเห็ดลมชิ้นที่ 2
            เป็นต้นไปจะนำไปเป็นรายได้ให้กับคยขายเห็ดลม
          </h3>
        </div>
      </div>
      <table style="margin-left: 500px">
        <thead class="flex px-10 text-center">
          <td class="p-5">ลำดับ</td>
          <td class="p-5">จำนวน</td>
          <td class="p-5">ราคา</td>
          <td class="p-5">รายการสินค้า</td>
        </thead>
        <tbody>
            <tr v-for="(a, index) in cart" :key="a.id.toSring()">
                <td>{{index}}</td>
            </tr>
          <tr v-for="(p, idx) in cart" :key="p.id.toString()" class="flex p-5">
            <td class="p-5">{{ idx + 1 }}</td>
            <td class="flex flex-inline">
              <button
                class="bg-green-500 p-5 text-white flex-1"
                @click="increment(p.id)"
              >
                +
              </button>
              <div class="flex flex-2 pt-5 p-3">{{ p.quantity }}</div>
              <button
                class="bg-red-500 p-5 text-white flex-3"
                @click="decrement(p.id)"
              >
                -
              </button>
            </td>
            <td class="p-5">{{ p.price }}</td>
            <td class="p-5">{{ p.name }}</td>
          </tr>
        </tbody>
      </table>

      <div>
        <h4 class="text-center">Total : {{ total }}</h4>
        <button @click="buy">Buy</button>
      </div>
    </div>
  </div>
</template>

<script>
import Cart from "./index"
export default {
}

</script>

<style>
</style>