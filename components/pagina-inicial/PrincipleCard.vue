<template>
  <div class="container mx-auto px-4">
    <div class="flex flex-wrap">
      <div class="pt-6 w-full px-4 text-center">
        <div
          class="
            relative
            flex flex-col
            min-w-0
            break-words
            bg-white
            w-full
            mb-8
            shadow-lg
            rounded-lg
          "
        >
          <div class="px-4 py-4 flex-auto">
            <div class="inline-flex items-center justify-center w-16 h-16">
              <img class="w-auto" :src="image" alt="Icon" />
            </div>
            <h6 class="text-xl font-semibold">{{ title }}</h6>
            <p class="mt-2 mb-4 text-gray-600 text-lg">
              {{ description }}
            </p>
            <div v-if="isValores" class="mt-2 mb-4 mx-6 text-lg text-gray-600 text-justify">
              1. A medicina espiritual como exercício legítimo e ético.<br />
              2. Entendimento da saúde integral do homem na visão espírita sob a
              égide de Jesus.<br />
              3. A ciência espírita, com sua metodologia de estudo, amplia a
              noção de saúde integral do homem e pode contribuir com a
              comunidade científica.
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PrincipleCard',
  props: {
    title: {
      type: String,
    },
    description: {
      type: String,
    },
    image: {
      type: String,
    },
    isValores: {
      type: Boolean,
    },
  },
}
</script>

<style>
</style>