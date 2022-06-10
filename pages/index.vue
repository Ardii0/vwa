<template>
  <div>
  <layout-container no-back>
    <section>
        <b-carousel
            :indicator="indicator"
            :indicator-background="indicatorBackground"
            :indicator-inside="indicatorInside"
            :indicator-mode="indicatorMode"
            :indicator-position="indicatorPosition"
            :indicator-style="indicatorStyle"
            :pause-hover="false"
            :pause-info="false">
        <b-carousel-item v-for="(item, i) in 6" :key="i">
                <!-- <section :class="`hero is-medium `"> -->
                    <!-- <div class="hero-body has-text-centered"> -->
            <b-image class="image" :src="getImgUrl(i)"></b-image>
                    <!-- </div> -->
                <!-- </section> -->
            </b-carousel-item>
        </b-carousel>
    </section>
      <p class="underline focus:decoration-wavy text-center mt-5">Beauty Essential</p>
    <div class="flex mt-5 mb-5 gap-5 ">
        <div class="container mx-auto">
          <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-3 gap-6 justify-items-center">
      <!-- <div class="border-2 bg-green-700  w-8 h-8 focus:outline-none"></div> -->
      <div class="bg-[#faecd4] rounded-full text-center ">
      <img class="w-60 display-flex" src="../assets/images/FentyBP.png" alt="FentyBeauty">
      <strong><h5>Skincare</h5></strong>
      <p>Start from $18.00</p>
      </div>
      <div class="bg-[#faecd4] rounded-[50%] text-center">
      <img class="w-60" src="../assets/images/FentyB.png" alt="FentyBeauty">
      <h5>Makeup</h5>
      <p>Start from $22.00</p>
      </div>
      <div class="bg-[#faecd4] rounded-[50%] text-center">
      <img class="w-60" src="../assets/images/FentyB.png" alt="FentyBeauty">
      <h5>Clean Eyes</h5>
      <p>Start from $18.00</p>
      </div>
          </div>
        </div>
    </div>
    <!-- <div class="container mt-5">
    <div class="grid grid-cols-4 gap-4"> -->
    <div class="mt-5 mb-5">
        <div class="h-96 w-full bg-[#faecd4] float-right">
          <div class="container mx-auto">
          <div class="grid grid-cols-2 md:grid-cols-2 lg:grid-cols-2 gap-6">

              <div>
      <img class="w-60 flex" src="../assets/images/FentyP.png" alt="FentyBeauty">
              </div>

              <div class="uppercase float-right mt-20 text-4xl leading-10">
                  <h1>order now and save up to 50%</h1>
              </div>
        </div>
        </div>
        </div>
    </div>
  </layout-container>
  </div>
</template>

<script>
export default {
    methods: {
      getImgUrl(value) {
          return `https://cdn.shopify.com/s/files/1/0028/8253/5533/files/Website_Banners_-_Up_to_50__off_desktop_1920x.jpg?v=1654145400`
      }
    },
    data() {
        return {
            indicator: true,
            indicatorInside: true,
            indicatorMode: 'hover',
            indicatorPosition: 'is-bottom',
            indicatorStyle: 'is-dots',
            carousels: [
                {   title: '1',
                    pict: 'https://cdn.shopify.com/s/files/1/0028/8253/5533/files/Website_Banners_-_Up_to_50__off_desktop_1920x.jpg?v=1654145400' },
                { pict: 'https://cdn.shopify.com/s/files/1/0028/8253/5533/files/Sweet_Repair_Launch_Desktop_1920x.jpg?v=1653535831' },
                { pict: 'Slide 3' },
                { pict: 'Slide 4' }
            ]
        }
    }
}
</script>