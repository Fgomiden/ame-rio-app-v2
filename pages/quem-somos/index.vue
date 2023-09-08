<template>
  <div class="py-2 bg-white">
    <div v-if="$fetchState.pending">
      <!-- por animação de loading -->
    </div>
    <div v-else class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2
        class="text-center text-3xl leading-8 font-extrabold tracking-tight text-gray-900"
      >
        Quem Somos
      </h2>
      <div id="diretoria">
        <h3 class="text-xl font-bold py-2">Diretoria</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 w-full">
          <div
            v-for="doctor in this.doctors.data.filter(
              (d) => d.attributes.field == 'Diretoria'
            )"
            :key="doctor.id"
          >
            <doctor-card :doctor="doctor" />
          </div>
        </div>
      </div>
      <div id="conselho-fiscal">
        <h3 class="text-xl font-bold py-2">Conselho Fiscal</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 w-full">
          <div
            v-for="doctor in this.doctors.data.filter(
              (d) => d.attributes.field == 'Conselho Fiscal'
            )"
            :key="doctor.id"
          >
            <doctor-card :doctor="doctor" />
          </div>
        </div>
      </div>
      <div id="responsavel">
        <h3 class="text-center text-xl font-bold py-5">
          Apresentação do responsável atual pela Associação
        </h3>
        <responsible-text/>
      </div>
      <div id="livros">
        <div>
          <h3 class="text-xl font-bold py-2">
            Autor de {{ this.books.data.length }} livros espíritas:
          </h3>
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 w-full">
            <div v-for="(book, index) in this.books.data" :key="index">
              <book-card :book="book" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DoctorCard from '~/components/quem-somos/DoctorCard.vue'
import BookCard from '~/components/quem-somos/BookCard.vue'
import ResponsibleText from '~/components/quem-somos/ResponsibleText.vue'
export default {
  components: { DoctorCard, BookCard, ResponsibleText },
  data() {
    return {
      doctors: {},
      books: {},
    }
  },
  async fetch() {
    this.doctors = await this.$axios.$get('api/doctors?sort[0]=id%3Aasc')
    this.books = await this.$axios.$get('/api/books?populate=*')
  },
  fetchOnServer: true,
}
</script>
