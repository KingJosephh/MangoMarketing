<template>
    <NavBar></NavBar>
    <section>
      <div class="container mt-5 mb-5">
        <div class="pb-5 border-bottom border-3 border-darkGray">
          <div class="row">
            <div class="col me-lg-5 mb-4 px-2">
              <img class="car-model8 rounded-4" src="../assets/fruit-img/sell.jpg">
            </div>
            <div class="col-lg-5">
              <h2 class="pb-3 mb-3 border-bottom border-darkGray border-2">{{ getProduct.title }}</h2>
              <div class="row mb-3">
                <p class="col-3 h5">商品資訊 : </p>
                <p class="col h5 overflow-auto" :style="{ height: '100px'}">{{ getProduct.content }}</p>
              </div>
              <div class="row pb-3 mb-3 border-bottom border-darkGray border-2">
                <p class="col-3 h5">業者資訊 : </p>
                <p class="col h5">{{ getProduct.description }}</p>
              </div>
              <p class="h3 mb-4">{{ getProduct.price }} / {{ getProduct.unit }}</p>
              <p class="h5">購買數量</p>
              <div class="col-4">
                <input type="number" class="form-control mb-3" v-model="amount">
              </div>
              <div class="col-4">
                <input type="button" class="btn btn-fire" value="加到購物車" @click="sendToCar">
              </div>
            </div>
        </div>
        </div>
        <div class="container mt-5">
          <div class="notice">
          <div class="content p-0 m-0">
            <div class="h5">公告事項說明</div>
            <ul class="notice-list p-0 list-unstyled">
              <li class="h6">1. 同一輛帳號訂購成功後三次未取貨者，視同黑名單車號，日後不得訂購。</li>
              <li class="h6">2. 訂購前請與業主確認是否需冷凍運送跟賞味期限是否可長途運送</li>
              <li class="h6">3. 商品腐爛、過期、嚴重碰撞或寄出錯誤除外不能退貨</li>
              <li class="h6 text-danger">★近日詐騙電話簡訊頻傳，為保障貴客戶自身權益暨防制詐騙，請貴客戶仔細閱讀以下事項，並隨時提高警覺。★</li>
            </ul>
          </div>
        </div>
        </div>
      </div>
    </section>
    <div class="display-5 shopping-fix">
      <i class="bi bi-cart4"></i>
    </div>
    <Footer></Footer>
    </template>

<script>
import NavBar from '@/components/CarNavBar.vue'
import Footer from '@/components/FooterPage.vue'

export default {
  data () {
    return {
      productList: [],
      getProduct: {},
      amount: 0,
      getProductId: ''
    }
  },
  components: {
    NavBar,
    Footer
  },
  methods: {
    getProductData () {
      const api = `${process.env.VUE_APP_API}api/${process.env.VUE_APP_PATH}/products/all`
      this.$http.get(api)
        .then((res) => {
          console.log(res)
          this.productList = res.data.products
          this.getShowOne()
        })
        .catch((err) => {
          console.log(err)
        })
    },
    getShowOne () {
      const productId = this.$route.params.carListId
      this.getProductId = productId
      this.getProduct = this.productList.find(item => item.id === productId) || {}
    },
    sendToCar () {
      if (this.amount !== 0) {
        const api = `${process.env.VUE_APP_API}api/${process.env.VUE_APP_PATH}/cart`
        this.$http.post(api, { data: { product_id: this.getProductId, qty: this.amount } })
          .then((res) => {
            console.log(res)
          })
          .catch((err) => {
            console.log(err)
          })
      }
    }
  },
  created () {
    this.getProductData()
  },
  mounted () {
    window.scrollTo(0, 0)
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@500&display=swap');
body {
  font-family: "Noto Sans TC", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
</style>
<!-- 製作加到購物車跟購物付款功能 -->
