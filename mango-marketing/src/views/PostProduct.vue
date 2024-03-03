<template>
    <section>
      <div class="container mt-4">
        <!-- <div class="d-flex justify-content-center">
          <img src="../assets/car-img/title3.png" alt="服務介紹">
        </div> -->
        <div class="d-flex mb-3 ms-2">
          <p>用戶 : aqaq6109@gmail.com</p>
        </div>
        <div class="row d-flex justify-content-center">
          <div class="col-4 py-2 ms-lg-2 mb-3 border-bottom border-3 border-dark d-flex justify-content-between">
            <i class="bi bi-shop display-5"></i>
            <i class="bi bi-clipboard2-minus display-5"></i>
            <i class="bi bi-truck display-5"></i>
            <i class="bi bi-cart-check display-5"></i>
          </div>
        </div>
        <div class="ms-2 mb-3">
          <button type="button" class="btn btn-fire ms-auto text-white fw-bold" @click="openModal(true)">新增產品</button>
        </div>
        <div class="row">
          <div class="col d-flex flex-wrap justify-content-start">
            <div class="card mx-2 mb-2 w-100 carBig" v-for="(item, index) in allProductList" :key="index">
              <img :src="`${item.imageUrl}`" class="card-img-top car-model7" alt="{{ item.title }}">
              <div class="card-body">
                <h5 class="card-title">產品 : {{ item.title }}</h5>
                <p class="card-text">內容物 : {{ item.content }}</p>
                <p class="card-text">描述 : {{ item.description }}</p>
              </div>
              <div class="card-footer bg-white d-flex justify-content-center">
                <a href="#" class="btn btn-outline-fire me-2" @click.prevent="openModal(false, item)">編輯</a>
                <a href="#" class="btn btn-outline-fire me-2" @click.prevent="openDel(item)">刪除</a>
                <a href="#" class="btn btn-outline-fire" @click.prevent="deleteProduct(item.id)">內容</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <nav aria-label="Page navigation example">
    <ul class="pagination d-flex justify-content-center mt-4">
      <li class="page-item" :class="{'disabled': currentPage === 1}"><a class="page-link" href="#" @click.prevent="goPage(currentPage-1)">Previous</a></li>
      <li class="page-item" v-for="(page, index) in pageTotal" :key="index" :class="{'active': currentPage === page}"><a class="page-link" href="#" @click.prevent="goPage(page)">{{ page }}</a></li>
      <li class="page-item" :class="{'disabled': currentPage === pageTotal}"><a class="page-link" href="#" @click.prevent="goPage(currentPage+1)">Next</a></li>
    </ul>
  </nav>
    <add-product ref="addProduct" :product="tempProduct" @update-condition="updateProduct"></add-product>
    <del-modal ref="delProduct" :delProduct="delProduct" @del-item="deleteProduct"></del-modal>
</template>
<script>

</script>
