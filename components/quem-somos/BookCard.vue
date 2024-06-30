<template>
  <div>
    <div
      class="flex flex-row shadow h-60 bg-white rounded-lg m-2"
    >
      <div class="flex">
        <img v-if="book.cover"
          :src="book.cover"
          alt="Capa Livro"
        />
      </div>
      <div class="flex flex-col w-80 md:w-52 justify-center py-4 mx-4 my-8">
        <h3 class="text-base font-medium text-gray-600">
          {{ book.name }}
        </h3>
        <h3 v-if="!book.available" class="text-base text-gray-600">
          (Esgotado)
        </h3>
        <h3 v-if="book.description" class="text-sm text-gray-600 pt-2">
          {{ book.description }}
        </h3>        
        <h3 v-if="book.publisher" class="text-base text-gray-600 pt-2">
          Editora: {{ book.publisher }}
        </h3>
        <h3 v-if="book.publisher_location" class="text-base text-gray-600">
          Local: {{ book.publisher_location }}
        </h3>   
        <h3 v-if="book.author" class="text-base text-gray-600">
          Autor: {{ book.author }}
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