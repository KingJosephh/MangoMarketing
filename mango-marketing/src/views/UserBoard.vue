<template>
    <div>
      <NavBar :page-title="pageTitleS"></NavBar>
      <TitleImg></TitleImg>
    <section class="mb-5">
      <div class="container">
        <div class="row row-cols-lg-2 row-cols-1 d-flex justify-content-center m-0">
          <div class="col">
            <div class="card bg-dark text-white rounded-4 show-card-detail mb-4">
              <router-link to="/page3/全部商品">
                <img src="../assets/fruit-img/shopping.jpg" class="card-img car-model6 rounded-4" alt="...">
                <div class="card-img-overlay rounded-4 d-flex justify-content-center align-items-center">
                  <h2 class="c2 text-center fw-bold text-white">購買商品</h2>
                  <div class="c1 card-img-overlay car-model6 rounded-4 gradient2">
                </div>
                </div>
              </router-link>
            </div>
          </div>
          <div class="col">
            <div class="card bg-dark text-white rounded-4 show-card-detail">
              <router-link to="/postProduct">
                <img src="../assets/fruit-img/sell.jpg" class="card-img car-model6 rounded-4" alt="...">
                <div class="card-img-overlay rounded-4 d-flex justify-content-center align-items-center">
                  <h2 class="c2 text-center fw-bold text-white">上架商品</h2>
                  <div class="c1 card-img-overlay car-model6 rounded-4 gradient2 p-0">
                </div>
                </div>
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section>
        <div class="container mb-5">
            <div class="d-flex justify-content-center pb-5">
                <img src="../assets/car-img/title2.png" alt="近期好車">
            </div>
            <div class="row" data-aos="fade-up" data-aos-duration="800" data-aos-delay="100">
                <div class="col-lg-12">
                    <div class="row g-4 m-0 row-cols-lg-4 row-cols-2 px-lg-0 px-4">
                        <div class="col">
                            <div class="card border-0 text-white show-card-detail rounded-4">
                              <router-link to="/page3/水果">
                                <img class="card-img car-model rounded-4" src="../assets/fruit-img/fruit.jpg" alt="fruit">
                                <div class="card-img-overlay d-flex flex-column justify-content-end">
                                    <div class="card-img-overlay gradient car-model rounded-4">
                                      <div class="d-flex justify-content-center h-100">
                                        <p class="d-flex align-items-lg-center my-auto h2 text-white fw-bold">水果</p>
                                      </div>
                                    </div>
                                </div>
                              </router-link>
                            </div>
                        </div>
                        <div class="col">
                            <div class="card border-0 text-white show-card-detail rounded-4">
                              <router-link to="/page3/蔬菜">
                                <img class="card-img car-model rounded-4" src="../assets/fruit-img/vegetable.jpg" alt="fruit">
                                <div class="card-img-overlay d-flex flex-column justify-content-end">
                                    <div class="card-img-overlay gradient car-model rounded-4">
                                      <div class="d-flex justify-content-center h-100">
                                        <p class="d-flex align-items-lg-center my-auto h2 text-white fw-bold">蔬菜</p>
                                      </div>
                                    </div>
                                </div>
                              </router-link>
                            </div>
                        </div>
                        <div class="col">
                            <div class="card border-0 text-white show-card-detail rounded-4">
                              <router-link to="/page3/肉品(原肉)">
                                <img class="card-img car-model rounded-4" src="../assets/fruit-img/origin meat.jpg" alt="fruit">
                                <div class="card-img-overlay d-flex flex-column justify-content-end">
                                    <div class="card-img-overlay gradient car-model rounded-4">
                                      <div class="d-flex justify-content-center h-100">
                                        <p class="d-flex align-items-lg-center my-auto h2 text-white fw-bold">肉品(原肉)</p>
                                      </div>
                                    </div>
                                </div>
                              </router-link>
                            </div>
                        </div>
                        <div class="col">
                            <div class="card border-0 text-white show-card-detail rounded-4">
                              <router-link to="/page3/肉品(加工)">
                                <img class="card-img car-model rounded-4" src="../assets/fruit-img/process meat.jpg" alt="fruit">
                                <div class="card-img-overlay d-flex flex-column justify-content-end">
                                    <div class="card-img-overlay gradient car-model rounded-4">
                                      <div class="d-flex justify-content-center h-100">
                                        <p class="d-flex align-items-lg-center my-auto h2 text-white fw-bold">肉品(加工)</p>
                                      </div>
                                    </div>
                                </div>
                              </router-link>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <div class="d-flex justify-content-center mt-5 mb-6">
        <router-link to="/page3">
            <button class="btn btn-fire text-white fw-bold"><p class="m-0 px-5">查看全部商品</p></button>
        </router-link>
    </div>
    <section>
        <div class="d-flex justify-content-center">
            <img src="../assets/car-img/title3.png" alt="服務介紹">
        </div>
    </section>
    <section>
        <div class="mt-4 mb-5">
            <div class="row px-6 m-0 row-cols-lg-4 row-cols-1">
                <div class="col">
                    <div class="row row-cols-lg-1 row-cols-2" data-aos="fade-up" data-aos-duration="800" data-aos-delay="300">
                        <div class="col-3 d-flex justify-content-center">
                            <img class="pb-lg-4 pb-0 car-model3" src="../assets/car-img/pag2/buy-car1.png" alt="網路選購好車">
                        </div>
                        <div class="col-9 d-flex flex-column justify-content-center ps-lg-0 ps-5">
                            <h3 class="fw-bold pb-lg-3 pb-2 m-0 text-lg-center text-start text-fire">網路訂購</h3>
                            <p class="text-lg-center text-start mb-5 fw-bold">線上購物<br>方便省時<br>購買在地農特產</p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="row row-cols-lg-1 row-cols-2" data-aos="fade-up" data-aos-duration="800" data-aos-delay="500">
                        <div class="col-3 d-flex justify-content-center">
                            <img class="pb-lg-4 pb-0 car-model3" src="../assets/car-img/pag2/buy-car2.png" alt="到店賞車">
                        </div>
                        <div class="col-9 d-flex flex-column justify-content-center ps-lg-0 ps-5">
                            <h3 class="fw-bold pb-lg-3 pb-2 m-0 text-lg-center text-start text-fire">公開透明</h3>
                            <p class="text-lg-center text-start mb-5 fw-bold">買家與賣家<br>直接接洽<br>不剝削農民</p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="row row-cols-lg-1 row-cols-2" data-aos="fade-up" data-aos-duration="800" data-aos-delay="700">
                        <div class="col-3 d-flex justify-content-center">
                            <img class="pb-lg-4 pb-0 car-model3" src="../assets/car-img/pag2/buy-car3.png" alt="喜提新車">
                        </div>
                        <div class="col-9 d-flex flex-column justify-content-center ps-lg-0 ps-5">
                            <h3 class="fw-bold pb-lg-3 pb-2 m-0 text-lg-center text-start text-fire">嚴格把關</h3>
                            <p class="text-lg-center text-start mb-5 fw-bold">食品經專業認證<br>人工智能檢測<br>專人現場篩檢</p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="row row-cols-lg-1 row-cols-2" data-aos="fade-up" data-aos-duration="800" data-aos-delay="900">
                        <div class="col-3 d-flex justify-content-center">
                            <img class="pb-lg-4 pb-0 car-model3" src="../assets/car-img/pag2/buy-car4.png" alt="幫助浪浪">
                        </div>
                        <div class="col-9 d-flex flex-column justify-content-center ps-lg-0 ps-5">
                            <h3 class="fw-bold pb-lg-3 pb-2 m-0 text-lg-center text-start text-fire">幫助農民</h3>
                            <p class="text-lg-center text-start mb-5 fw-bold">幫農民曝光自家產品<br>操作簡單<br></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section>
        <div class="bg-img-size4" :style="{ backgroundImage: `url(${require('../assets/car-img/f-page4.jpg')})`}">
            <div class="row m-0">
              <div class="col-lg-4 col-12 text-white d-flex flex-column justify-content-center align-items-center" data-aos="fade-up" data-aos-duration="800" data-aos-delay="700">
                <div class="row d-flex flex-column">
                  <div class="col-lg-12 col-0 d-lg-block d-none">
                    <img src="../assets/car-img/shop1.jpg" :style="{height:'400px'}" class="car-model4 mt-5">
                  </div>
                  <div class="col">
                    <h3 class="fw-bold text-white text-start mt-4">台中總店</h3>
                    <h5>電話:02-456851</h5>
                    <h5>地址:台中市西區民權路789號</h5>
                    <i class="bi bi-line h5 me-3 text-fire"></i><i class="bi bi-facebook h5 me-3 text-fire"></i><a href="https://www.instagram.com/mango_treeeee/"><i class="bi bi-instagram h5 me-3 text-fire"></i></a>
                  </div>
                </div>
              </div>
              <div class="col-lg-4 col-12 text-white d-flex flex-column justify-content-center align-items-center" data-aos="fade-up" data-aos-duration="800" data-aos-delay="700">
                <div class="row d-flex flex-column">
                  <div class="col-lg-12 col-0 d-lg-block d-none">
                    <img src="../assets/car-img/shop1.jpg" :style="{height:'400px'}" class="car-model4 mt-5">
                  </div>
                  <div class="col">
                    <h3 class="fw-bold text-white text-start mt-4">桃園中壢店</h3>
                    <h5>電話:01-458123</h5>
                    <h5>地址:桃園市中壢區中大路456號</h5>
                    <i class="bi bi-line h5 me-3 text-fire"></i><i class="bi bi-facebook h5 me-3 text-fire"></i><i class="bi bi-instagram h5 me-3 text-fire"></i>
                  </div>
                </div>
              </div>
              <div class="col-lg-4 col-12 text-white d-flex flex-column justify-content-center align-items-center" data-aos="fade-up" data-aos-duration="800" data-aos-delay="700">
                <div class="row d-flex flex-column">
                  <div class="col-lg-12 col-0 d-lg-block d-none">
                    <img src="../assets/car-img/shop1.jpg" :style="{height:'400px'}" class="car-model4 mt-5">
                  </div>
                  <div class="col">
                    <h3 class="fw-bold text-white text-start mt-4">高雄建工店</h3>
                    <h5>電話:07-12560</h5>
                    <h5>地址:高雄市三民區建工路123號</h5>
                    <i class="bi bi-line h5 me-3 text-fire"></i><i class="bi bi-facebook h5 me-3 text-fire"></i><i class="bi bi-instagram h5 me-3 text-fire"></i>
                  </div>
                </div>
              </div>
            </div>
        </div>
    </section>
    <div class="display-4 shopping-fix">
      <i class="bi bi-cart4"></i>
    </div>
        <Footer></Footer>
    </div>
</template>

<script>
import NavBar from '@/components/CarNavBar.vue'
import Footer from '@/components/FooterPage.vue'
import TitleImg from '@/components/UserBoardSwiper.vue'
import 'swiper/css'
import 'swiper/css/free-mode'
import 'swiper/css/pagination'
import 'swiper/css/navigation'
import '../assets/components/style1.css'

// import required modules
export default {
  components: {
    NavBar,
    Footer,
    TitleImg
  },
  data () {
    return {
      allList: [],
      topFive: [],
      topFiveEarly: [],
      pageTitleS: '首頁'
    }
  },
  methods: {
    getAllProduct () {
      const api = `${process.env.VUE_APP_API}api/${process.env.VUE_APP_PATH}/products/all`
      this.isLoading = true
      this.$http.get(api)
        .then((res) => {
          console.log(res)
          this.allList = res.data.products
          // this.isLoading = false
        }).catch((err) => {
          console.log(err)
        })
    }
  },
  created () {
    this.getAllProduct()
  },
  mounted () {
    window.scrollTo(0, 0)
  }
}
</script>
<!-- 改切版參考pintrest圖片 -->
