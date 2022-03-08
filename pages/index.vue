<template>
  <div class="bg-yellow-50 w-full h-full">
    <div>
      <div
        class="px-4 py-16 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 lg:py-20"
      >
        <p
          class="mb-2 text-xs font-semibold tracking-wide text-gray-600 uppercase sm:text-center"
        >
          25 Jan 2002
        </p>
        <div class="max-w-xl mb-5 md:mx-auto sm:text-center lg:max-w-2xl">
          <div class="mb-4">
            <a
              href="/simp"
              aria-label="Article"
              class="inline-block max-w-lg font-sans text-3xl font-extrabold leading-none tracking-tight text-black transition-colors duration-200 hover:text-deep-purple-accent-700 sm:text-4xl"
            >
              เห็ดลม
            </a>
          </div>
          <p class="text-base text-gray-700 md:text-lg">
            เวลาเหงาเปล่าเปลี่ยวใจ เมื่อเพื่อนหรือบทเพลงไม่อาจสงบความเหงาในใจได้
            คุณสนใจมาลองฟังเรื่องเล่าจากเหล่านิรนามมั้ย ความรัก
            ความสยองขวัญและความตื่นเต้นกำลังรอคุณเข้ามาฟัง
            เติมเต็มหัวใจของคุณด้วยสิ่งนี้สิ
          </p>
        </div>
        <div class="mb-10 sm:text-center">
          <a href="/" aria-label="Author" class="inline-block mb-1">
            <img
              alt="avatar"
              src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=2&amp;h=750&amp;w=1260"
              class="object-cover w-10 h-10 rounded-full shadow-sm"
            />
          </a>
          <div>
            <a
              href="/"
              aria-label="Author"
              class="font-semibold text-gray-800 transition-colors duration-200 hover:text-deep-purple-accent-700"
              >นิรนาม</a
            >
            <p class="text-sm font-medium leading-4 text-gray-600">
              ถ้าอยากรู้จักหนุ่มสาวนิรนามเหล่านี้มาอีกล่ะก็
            </p>
          </div>
        </div>
        <div class="sm:text-center">
          <a
            href="https://github.com/Jenitsata"
            aria-label=""
            class="inline-flex items-center font-semibold transition-colors duration-200 text-deep-purple-accent-400 hover:text-red-400"
            >Github</a
          >
        </div>
      </div>
    </div>
    <div>
      <div
        style="margin-left: 200px"
        class="relative px-4 py-16 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 lg:py-20"
      >
        <div
          class="absolute inset-x-0 top-0 items-center justify-center hidden overflow-hidden md:flex md:inset-y-0"
        >
          <svg viewBox="0 0 88 88" class="w-full max-w-screen-xl text-red-100">
            <circle fill="currentColor" cx="44" cy="44" r="15.5"></circle>
            <circle
              fill-opacity="0.2"
              fill="currentColor"
              cx="44"
              cy="44"
              r="44"
            ></circle>
            <circle
              fill-opacity="0.2"
              fill="currentColor"
              cx="44"
              cy="44"
              r="37.5"
            ></circle>
            <circle
              fill-opacity="0.3"
              fill="currentColor"
              cx="44"
              cy="44"
              r="29.5"
            ></circle>
            <circle
              fill-opacity="0.3"
              fill="currentColor"
              cx="44"
              cy="44"
              r="22.5"
            ></circle>
          </svg>
        </div>
        <div class="relative grid gap-5 sm:grid-cols-2 lg:grid-cols-4">
          <div
            class="flex flex-col overflow-hidden text-left transition-shadow duration-200 bg-white rounded shadow-xl group hover:shadow-2xl"
            v-for="product in products"
            :key="product.id.toString()"
          >
            <div class="p-5">
              <div
                class="flex items-center justify-center w-10 h-10 mb-4 rounded-full bg-red-50"
              >
                <button
                  class="flex text-center text-xl text-red-500"
                  v-if="!product.cart"
                  @click="add(product)"
                >
                  +
                </button>
                <button
                  v-if="product.cart"
                  @click="add(product)"
                  :disabled="product.cart"
                  href="#"
                  class="flex text-center text-xl text-red-500"
                >
                  O
                </button>
              </div>
              <p class="mb-2 font-bold">{{ product.title }}</p>
              <p class="text-sm leading-5 text-gray-900">
                {{ product.subtitle }}
              </p>
              <p>฿ {{ product.price }}</p>
            </div>
            <div
              class="w-full h-1 ml-auto duration-300 origin-left transform scale-x-0 bg-deep-purple-accent-400 group-hover:scale-x-100"
            ></div>
          </div>
        </div>
      </div>
    </div>
    <div>
      <div class="mx-auto p-16" style="max-width: 800px">
        <div class="flex items-center justify-between mb-8 px-3">
          <div>
            <span class="text-2xl">Wind Mushroom #</span>: 0001-2019<br />
            <span>Date</span>: January 1st 2019<br />
          </div>
          <div class="text-right">
            <img src="~/assets/mushroom.png" class="w-10" />
          </div>
        </div>

        <div class="flex justify-between mb-8 px-3">
          <div>
            Pixel &amp; Tonic<br />
            919 NW Bond St. Ste 203<br />
            Bend, OR 97703 USA<br />
            hello@pixelandtonic.com<br />
            +1 855-700-5115
          </div>
          <div class="text-right">
            Wind Mushroom Company<br />
            Street 12<br />
            10000 City<br />
            wind_mushroom@yoursite.com
          </div>
        </div>

        <div class="border border-t-2 border-gray-200 mb-8 px-3"></div>

        <div class="mb-8 px-3">
          <p>
            จำนวนเรื่องราวที่ถูกซื้อมากกว่า 2
            ขึ้นไปจะมอบกำไรให้กับผู้ขายเห็ดลมโดยตรงโดยไม่หักค่าใช้จ่ายเว็บไซต์
          </p>
        </div>
        <table>
          <thead class="flex px-10 text-center">
            <td class="p-5">#</td>
            <td class="p-5">Quantity</td>
            <td class="p-5">Price</td>
            <td class="p-5">Product Name</td>
          </thead>
          <tbody>
            <tr
              v-for="(p, idx) in cart"
              :key="p.id.toString()"
              class="flex justify-between mb-4 bg-gray-200 px-3 py-2"
            >
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
              <td class="p-5">{{ p.title }}</td>
            </tr>
          </tbody>
        </table>
        <div class="flex justify-between items-center mb-2 px-3">
          <div class="text-2xl leading-none"><span class="">Total</span>:</div>
          <div class="text-2xl text-right font-medium">฿ {{total}}</div>
        </div>
        <div class="mb-8 px-3">
          <button @click="buy" class=" bg-green-500 px-5 p-1">Buy</button>
        </div>
        <div class="mb-8 text-4xl text-center px-3">
          <span>Thank you!</span>
        </div>
        <div class="text-center text-sm px-3">
          wind_mushroom@yourdomain.com ∖ www.yourdomain.com
        </div>
      </div>
    </div>
  </div>
</template>


<script lang="js">
  export default {
    name: "Cart",
    props: {
      msg: String,
    },
    data() {
      return {
        ticket: {
          products: null,
          total: 0,
        },
        counter: 0,
        products: [
          {
            id: 1,
            title: "เรื่องสยองขวัญในห้องวิศวกรรมซอฟต์แวร์",
            subtitle: "เมื่อเข้าไปในห้องแล้วที่พื้นหญ้าเทียมนั่นมีวิญญาณของคนสอบโปรเจคอยู่ ว่ากันว่าถ้าเข้าไปทักจะถูกสาปเอาได้",
            price: 20,
            cart: false,
            quantity: 1,
          },
          {
            id: 2,
            title: "อ่างหลวงเลิฟเลิฟ",
            subtitle: "เขาลือกันว่าถ้าไปที่อ่างหลางมีคนที่สามารถทำให้ความรักสมหวังได้ อยากรู้รึเปล่าว่าต้องทำยังไง?...",
            price: 20,
            cart: false,
            quantity: 1,
          },
          {
            id: 3,
            title:"ร้านอร่อยในม.พะเยามีจริง",
            subtitle: "รายชื่อร้านไม่อร่อยในม.พะเยาถูกคัดออกมาให้เห็นเต็มตาแล้ว! และร้านอร่อยนั่นน่ะคือ...!",
            price: 30,
            cart: false,
            quantity: 1,
          },
          {
            id: 4,
            title: "ผมไปเข้าป่าบนม.พะเยามาครับ",
            subtitle:"มีเรื่องจะเล่าเยอะเลยครับ ถ้าได้ฟังแล้วคุณจะต้องตื่นตะลึงแน่นอน จะเรื่องนกยูงไหม้ เต่าสุก ศพสุนัข อืมๆ เยอะเลยครับ",
            price: 10,
            cart: false,
            quantity: 12,
          },
          {
            id: 5,
            title: "Vtuber สังกัดม.พะเยา ปล่อบภาพวิชวลแล้ว!",
            subtitle:"มาชมภาพวิชวลและข้อมูลสาวเจ้านี้กันเถอะครับ น้องเอื้องคำ จะเป็น Vtuber แบบไหนกันนะ",
            price: 5,
            cart: false,
            quantity: 1,
          },
          {
            id: 6,
            title:"กาดวันศุกร์13สุดสยอง",
            subtitle: "กาดที่จัดตรงกับวันที่ 13 มีเรื่องเล่าสุดประหลาดให้คุณรับฟัง 10 เรื่องจุใจ",
            price: 3,
            cart: false,
            quantity: 1,
          },
          {
            id: 7,
            title:"ผู้หญิงหอ 11 น่ารักมากมาส่องสาวๆกัน",
            subtitle: "(ขออนุญาติเจ้าตัวแล้ว) มาเลยครับ แจกเฟส แจกไอจี แจกไลน์ เปิดแกนวาร์ปไปหาเหล่านางฟ้ากันครับผม",
            price: 15,
            cart: false,
            quantity: 1,
          },
          {
            id: 8,
            title:"ICTตอนเที่ยงคืน",
            subtitle: "ช่วงเวลาที่ยามเปลี่ยนกะ จะเป็นช่วงเวลาออกล่าของสิ่งมีชีวิตประหลาด แต่ถ้าคุณกล้าเข้าไปหามันได้แล้วขอพร มันจะช่วยให้คุณผ่านการสอบได้อย่างไม่น่าเชื่อ",
            price: 10,
            cart: false,
            quantity: 1,
          },
        ],
        cart: [],
        fields: ["#", "remove", "title", "quantity", "price"],
        
      }; // data return
    },
    methods: {
      add(product) {
        this.products[product.id - 1].cart = true;
        this.cart.push(product);
        // this.counter++;

      },
      increment(id) {
        const idx = this.cart.findIndex(c => c.id === id)
        this.cart[idx].quantity++

      },
      decrement(id) {
        const idx = this.cart.findIndex(c => c.id === id)
        if (this.cart[idx].quantity <= 0) return
        this.cart[idx].quantity--
      },
      buy() {
        alert("Purchase Complete");
      },
    },
    computed: {
      total() {
        let t = 0;
        for (let index = 0; index < this.cart.length; index++) {
          t += this.cart[index].price * this.cart[index].quantity;
        }
        return t.toFixed(2);
      },
    },
    entering() {
      
    }
  }
</script>

<style>
.group:hover .group-hover\:block {
  display: block !important;
}
</style>
