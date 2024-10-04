<template>
    <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 lg:px-6">
      <div
        class="mx-auto max-w-screen-md text-center mb-8 lg:mb-12"
        data-aos="fade-up"
        data-aos-duration="500"
      >
        <h2 class="mb-4 text-4xl tracking-tight font-bold text-[#0B132A]">
          Trusted by Thousands
          <br />of Happy Customer
        </h2>
        <p class="mb-5 font-light text-[#4F5665] sm:text-xl">
          These are the stories of our customers who have joined us with great
          <br />pleasure when using this crazy feature.
        </p>
      </div>
    </div>
    <div class="testimonial-slider" data-aos="fade-up" data-aos-duration="500">
      <swiper
        :breakpoints="{
          640: { slidesPerView: 1, spaceBetween: 10 },
          768: { slidesPerView: 2, spaceBetween: 20 },
          1024: { slidesPerView: 3, spaceBetween: 30 }
        }"
        loop
        :navigation="{ nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev' }"
        pagination
      >
        <swiper-slide v-for="(testimonial, index) in testimonials" :key="index">
          <div class="testimonial-card">
            <div class="user-info">
              <img :src="testimonial.image" alt="User Image" class="user-image" />
              <div class="user-details">
                <h3>{{ testimonial.name }}</h3>
                <p>{{ testimonial.location }}</p>
              </div>
              <p class="rating">
                {{ testimonial.rating }}
                <span class="star">⭐</span>
              </p>
            </div>
            <blockquote>{{ testimonial.quote }}</blockquote>
          </div>
        </swiper-slide>
      </swiper>
  
      <!-- ناوبری سفارشی برای فلش ها -->
      <div class="swiper-navigation">
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>
    </div>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from "swiper/vue";
  import "swiper/swiper-bundle.css";
  
  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
        testimonials: [
          {
            name: "Viezh Robert",
            location: "Warsaw, Poland",
            rating: 4.5,
            quote:
              "Wow... I am very happy to use this VPN service; it has been a life-changer in terms of protecting my online privacy and enabling me to access services safely.",
            image: "/images/viez_robert.png"
          },
          {
            name: "Yessica Christy",
            location: "Shanxi, China",
            rating: 4.5,
            quote:
              "I like it because I like to travel far, and this VPN makes it so easy to connect from anywhere. It’s a great service for frequent travelers.",
            image: "/images/yessica_christy.png"
          },
          {
            name: "Kim Young Jou",
            location: "Seoul, South Korea",
            rating: 4.5,
            quote:
              "This is very unusual for my business, and I appreciate the high level of security and seamless connection it provides me.",
            image: "/images/lim_young_jou.png"
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .testimonial-card {
    border: 1px solid #eee;
    padding: 20px;
    border-radius: 10px;
    text-align: left;
  }
  
  .user-info {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 15px;
  }
  
  .user-image {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    object-fit: cover;
    margin-right: 15px;
  }
  
  .user-details {
    text-align: left;
    flex-grow: 1;
  }
  
  .user-details h3 {
    font-size: 1.1em;
    font-weight: bold;
    margin: 0;
    color: #333;
  }
  
  .user-details p {
    font-size: 0.9em;
    color: #777;
    margin: 5px 0 0;
  }
  
  .rating {
    display: flex;
    align-items: center;
    font-size: 1em;
    color: #333;
  }
  
  .star {
    color: #fea250;
    margin-left: 5px;
  }
  
  blockquote {
    font-style: italic;
    color: #666;
    margin-top: 10px;
  }
  
  .testimonial-slider {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
    padding-bottom: 60px; /* فضای کافی برای دکمه‌های ناوبری */
  }
  
  .swiper-navigation {
    display: flex;
    justify-content: flex-end; /* قرار دادن دکمه‌ها در سمت راست */
    align-items: center;
    margin-top: 20px; /* فاصله بین ناوبری و کارت‌های اسلاید */
    position: absolute;
    bottom: 10px; /* موقعیت دکمه‌ها پایین کارت‌ها */
    left: 50%;
    gap: 0;
  }
  
  .swiper-button-prev,
  .swiper-button-next {
    border-radius: 50%;
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: xx-large;
    color: #fff;
    transform: rotateZ(180deg);
 
    border: 2px solid transparent;
  }
  
  .swiper-button-prev {
    background-color: #f53838;
  }
  
  .swiper-button-next {
    background-color: #ffffff;
    border-color: #f53838;
    color: #f53838;
  }
  
  .swiper-button-prev::after,
  .swiper-button-next::after {
    font-size: 20px;
  }
  </style>
  