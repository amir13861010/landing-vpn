<template>
  <div class="w-full mx-auto flex justify-center items-center mt-10" data-aos="fade-up" data-aos-duration="500">
    <div class="bg-white p-6 border w-full max-w-[1140px] h-auto sm:h-[200px] rounded-lg shadow-md flex flex-col sm:flex-row space-y-6 sm:space-y-0 sm:space-x-6 custom-size relative">
      <div class="flex-1 flex justify-center items-center p-3">
        <img src="/images/icon-user.png" alt class="w-[45px] h-[45px] sm:w-[55px] sm:h-[55px] mr-4" />
        <div>
          <h3 class="text-xl sm:text-2xl font-bold">+90</h3>
          <p class="text-gray-600">Users</p>
        </div>
      </div>
      
      <div class="flex-1 flex justify-center items-center p-3 border-t sm:border-t-0 sm:border-l sm:border-r px-6">
        <img src="/images/location.png" alt class="w-[45px] h-[45px] sm:w-[55px] sm:h-[55px] mr-4" />
        <div>
          <h3 class="text-xl sm:text-2xl font-bold">+90</h3>
          <p class="text-gray-600">Locations</p>
        </div>
      </div>
      
      <div class="flex-1 flex justify-center items-center p-3">
        <img src="/images/Server.png" alt class="w-[45px] h-[45px] sm:w-[55px] sm:h-[55px] mr-4" />
        <div>
          <h3 class="text-xl sm:text-2xl font-bold">+90</h3>
          <p class="text-gray-600">Servers</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
/* تنظیمات مرز برای حالت دسکتاپ */
.border-l {
  border-left: 1px solid #e5e7eb;
}
.border-r {
  border-right: 1px solid #e5e7eb;
}

/* تنظیمات مرز برای حالت موبایل */
@media (max-width: 640px) {
  .border-t {
    border-top: 1px solid #e5e7eb;
  }
}
</style>
