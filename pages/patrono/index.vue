<template>
  <div class="py-2 bg-white">
    <div class="max-w-xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2
        class="
          text-center text-3xl
          leading-8
          font-extrabold
          tracking-tight
          text-gray-900
        "
      >
        Patrono
      </h2>
    </div>
    <div class="mx-auto">
      <div class="flex justify-center">
        <div class="px-5 md:px-40">
          <div class="flex flex-col text-center">
            <h3 class="font-bold text-xl">Biografia do patrono da AME-RIO</h3>
          </div>
          <div class="flex flex-col py-4">
            <img
              src="https://res.cloudinary.com/ame-rio/image/upload/v1650556506/bezerra-de-menezes.jpg"
              class="w-full h-52 object-contain"
              alt="Dr. Bezerra de Menezes"
            />
          </div>
        </div>
      </div>
      <patron-text />
    </div>
  </div>
</template>
<script>
import PatronText from '~/components/patrono/PatronText.vue'
export default {
  components: { PatronText },
}
</script>