<template>
  <div>
    <div
      class="flex flex-row shadow h-44 bg-white rounded-lg cursor-pointer m-2"
    >
      <img
        class="flex object-cover w-1/3"
        :src="
          book.attributes.cover.data
            ? book.attributes.cover.data.attributes.name
            : './icons/book-open.svg'
        "
        alt="Capa Livro"
      />
      <div class="px-1 py-4">
        <h3 class="text-base font-medium text-gray-800">
          {{ book.attributes.name }}
        </h3>
        <h3 class="text-base text-gray-600 pt-2">
          Editora: {{ book.attributes.publisher }}
        </h3>
        <h3 class="text-base text-gray-600">
          Local: {{ book.attributes.publisher_location }}
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