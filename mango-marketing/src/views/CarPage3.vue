<template>
    <NavBar :page-title="pageTitleS"></NavBar>
    <header class="min-vh-2-40 position-relative">
        <div class="position-absolute bg-attachment-fixed bg-img-size-2 mb-2" :style="{ backgroundImage: `url(${require('@/assets/car-img/pag2/pg2Car.jpg')})`, top: 0, right: 0, bottom: 0, left: 0, height: '230px'}"></div>
        <div class="position-absolute top-50 start-50 translate-middle text-center text-secondary">
            <p class="display-1 fw-bold">商品 列表</p>
            <hr class="mb-1 mx-n3">
        </div>
    </header>
    <!-- <section>
        <div class="d-flex justify-content-center pb-5">
            <img src="../assets/car-img/title2.png" alt="熱門車款">
        </div>
    </section> -->
    <!-- <div class="row m-0">
      <div class="col-lg-2">
      </div>
      <div class="col pe-lg-10 mb-4 ms-lg-6 d-flex justify-content-center justify-content-lg-start">
        <button type="button" class="btn btn-fire text-white fw-bold animate__animated animate__pulse animate__infinite" @click="openModal">篩選條件</button>
      </div>
    </div> -->
    <section>
        <div class="row m-0 px-lg-6 px-1 d-flex flex-column flex-lg-row">
          <div class="col-lg-2 d-lg-block d-none">
                <div class="row gy-3">
                    <div class="row d-flex flex-column">
                        <div class="col">
                            <div class="col">
                                <p class="h4 text-lg-start text-center pb-3 mt-3"></p>
                            </div>
                        </div>
                        <div class="col ps-lg-2 ps-6 mb-3">
                            <div class="row d-flex flex-lg-column flex-row gy-lg-3">
                                <div class="col d-flex ds-dash-father ds-hover-father">
                                    <h5 class="position-absolute text-fire ds-dash">-</h5>
                                    <h5 class="position-relative ds-hover text-nowrap" :class="{'text-fire': option === '全部商品'}" @click.prevent="getOption('全部商品')">全部商品</h5>
                                </div>
                                <div class="col d-flex ds-dash-father ds-hover-father">
                                    <h5 class="position-absolute text-fire ds-dash">-</h5>
                                    <h5 class="position-relative ds-hover text-nowrap" :class="{'text-fire': option === '蔬菜'}" @click.prevent="getOption('蔬菜')">蔬菜</h5>
                                </div>
                                <div class="col d-flex ds-dash-father ds-hover-father">
                                    <h5 class="position-absolute text-fire ds-dash">-</h5>
                                    <h5 class="position-relative ds-hover text-nowrap" :class="{'text-fire': option === '水果'}" @click.prevent="getOption('水果')">水果</h5>
                                </div>
                                <div class="col d-flex ds-dash-father ds-hover-father">
                                    <h5 class="position-absolute text-fire ds-dash">-</h5>
                                    <h5 class="position-relative ds-hover text-nowrap" :class="{'text-fire': option === '肉品(原肉)'}" @click.prevent="getOption('肉品(原肉)')">肉品(原肉)</h5>
                                </div>
                                <div class="col d-flex ds-dash-father ds-hover-father">
                                    <h5 class="position-absolute text-fire ds-dash">-</h5>
                                    <h5 class="position-relative ds-hover text-nowrap" :class="{'text-fire': option === '肉品(加工)'}" @click.prevent="getOption('肉品(加工)')">肉品(加工)</h5>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
          </div>
            <div class="col">
              <!-- <div class="col-10">
                <div class="mb-4 row d-flex">
                  <p class="col-3 text-center mt-2 h5"><i class="bi bi-search"></i></p>
                  <div class="col ps-0">
                    <input type="text" class="form-control me-lg-2 ms-4" placeholder="請輸入關鍵字" v-model="option">
                  </div>
                </div>
              </div> -->
              <div class="col-lg-4 col-10 mb-2 d-flex justify-content-lg-start justify-content-center">
                <div class="row">
                  <div class="col-lg-3 col-3 mt-2 ms-lg-2 ms-5"><p>搜尋:</p></div>
                  <div class="col">
                    <input type="text" class="form-control me-lg-2 ms-4" placeholder="請輸入關鍵字" v-model="option">
                  </div>
                </div>
              </div>
              <div class="col-10 d-lg-none d-block mb-4 mx-auto">
                <select name="option" id="option" class="form-select border-bottom" v-model="option">
                  <option value="全部商品" selected>全部商品</option>
                  <option value="蔬菜">蔬菜</option>
                  <option value="水果">水果</option>
                  <option value="肉品(原肉)">肉品(原肉)</option>
                  <option value="肉品(加工)">肉品(加工)</option>
                </select>
              </div>
                <div class="mb-5">
                    <div class="row m-0 row-cols-lg-3 row-cols-2 px-lg-0 px-2">
                        <div class="col mt-0 mb-3" v-for="(item, index) in getPageData" :key="index">
                          <router-link :to="{name:'page6', params:{carListId:item.id}}">
                            <div class="card border-0 text-white show-card-detail rounded-4">
                                <img class="card-img car-model rounded-4" :src="`${item.imageUrl}`" :alt="item.title">
                                <div class="card-img-overlay d-flex flex-column justify-content-end">
                                    <p class="c2 fw-bold mb-0">產品</p>
                                    <p class="c2 m-0 title">{{ item.title }}</p>
                                    <div class="c2 d-lg-flex justify-content-between">
                                      <!-- <div class="c2 d-flex justify-content-lg-between">
                                        <i class="bi bi-fire text-fire"></i>
                                        <p class="m-0">{{ item.fire }}</p>
                                      </div> -->
                                      <p class="m-0 text-white h4">售價: {{ item.price }} / {{ item.unit }}</p>
                                    </div>
                                    <div class="c1 card-img-overlay gradient car-model rounded-4">
                                      <div class="d-flex justify-content-center h-100">
                                        <p class="d-flex align-items-lg-center my-auto h5 text-white fw-bold d-lg-block d-none">點我</p>
                                      </div>
                                    </div>
                                </div>
                            </div>
                          </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <nav aria-label="Page navigation example" class="d-flex justify-content-center">
          <ul class="pagination">
            <li class="page-item" :class="{'disabled': currentPage == 1}"><a class="page-link border-0 text-fire" href="#" @click.prevent="clickGotPage(currentPage-1)">Previous</a></li>
            <li class="page-item" v-for="(page, index) in countPage" :key="index" :class="{'active': currentPage == page}"><a class="page-link border-0 text-fire" href="#" @click.prevent="clickGotPage(page)">{{ page }}</a></li>
            <li class="page-item" :class="{'disabled': currentPage == countPage}"><a class="page-link border-0 text-fire" href="#" @click.prevent="clickGotPage(currentPage+1)">Next</a></li>
          </ul>
        </nav>
        <div v-if="!showTop" class="display-5 shopping-fix" @click="goTop">
          <i class="bi bi-arrow-up"></i>
        </div>
        <div @scroll="getScroll"></div>
    </section>
        <Footer></Footer>
    </template>

<script>
import NavBar from '@/components/CarNavBar.vue'
import Footer from '@/components/FooterPage.vue'
export default {
  components: {
    NavBar,
    Footer
  },
  data () {
    return {
      productList: [],
      filterProduct: [],
      pageTitleS: '熱門車款',
      currentPage: 1,
      perPage: 18,
      option: '全部商品',
      showTop: false
    }
  },
  watch: {
    option: {
      handler () {
        this.getOptionProduct(this.option)
      }
    }
  },
  computed: {
    countPage () {
      return this.filterProduct.length > 0 ? Math.ceil(this.filterProduct.length / this.perPage) : 0
    },
    getPageData () {
      return this.filterProduct.length > 0
        ? this.filterProduct.slice((this.currentPage - 1) * this.perPage, (this.currentPage * this.perPage))
        : []
    }
  },
  methods: {
    getProduct () {
      const api = `${process.env.VUE_APP_API}api/${process.env.VUE_APP_PATH}/products/all`
      this.$http.get(api)
        .then((res) => {
          console.log(res)
          this.productList = res.data.products
          this.getOptionProduct(this.option)
        })
        .catch((err) => {
          console.log(err)
        })
    },
    clickGotPage (page) {
      this.currentPage = page
      window.scrollTo(0, 0)
    },
    getOption (aa) {
      this.option = aa
    },
    getOptionId () {
      const optionId = this.$route.params.productListId
      this.option = optionId
    },
    getOptionProduct (aa) {
      if (aa !== '全部商品' && aa !== '蔬菜' && aa !== '水果' && aa !== '肉品(原肉)' && aa !== '肉品(加工)') {
        this.filterProduct = this.productList.filter(item => item.title.includes(aa))
      } else if (aa === '全部商品') {
        this.filterProduct = this.productList
      } else {
        this.filterProduct = this.productList.filter(item => item.category.includes(aa))
      }
    },
    goTop () {
      window.scroll(0, 0)
    },
    getScroll () {
      // const aa = this.$refs.catchScroll.scrollTop
      const bb = window.scrollY
      bb !== 0 ? this.showTop = false : this.showTop = true
    }
  },
  mounted () {
    this.getProduct()
    this.getOptionId()
    window.scrollTo(0, 0)
    window.addEventListener('scroll', this.getScroll)
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
<!-- 更改手機板參考4%版型
製作page6也參考4%版型 -->
