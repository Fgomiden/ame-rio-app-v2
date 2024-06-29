<template>
  <div>
    <div
      class="flex flex-row shadow h-48 bg-white rounded-lg m-2"
    >
      <img v-if="book.cover"
        class="flex object-cover w-1/3"
        :src="book.cover"
        alt="Capa Livro"
      />
      <div class="flex flex-col justify-center py-4 mx-4 my-8">
        <h3 class="text-base font-medium text-gray-800">
          {{ book.name }}
        </h3>
        <h3 v-if="book.available == 0" class="text-base text-gray-600">
          (Esgotado)
        </h3>
        <h3 class="text-base text-gray-600 pt-2">
          {{ book.description }}
        </h3>        
        <h3 class="text-base text-gray-600 pt-2">
          Editora: {{ book.publisher }}
        </h3>
        <h3 class="text-base text-gray-600">
          Local: {{ book.publisher_location }}
        </h3>        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BookCard',
  props: {
    book: Object,
  },
}
</script>