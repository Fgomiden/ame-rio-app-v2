<template>
  <div class="py-2 bg-white">
    <div v-if="$fetchState.pending">
      <!-- por animação de loading -->
    </div>
    <div v-else class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2
        class="
          text-center text-3xl
          leading-8
          font-extrabold
          tracking-tight
          text-gray-900
        "
      >
        Quem Somos
      </h2>
      <div id="diretoria">
        <h3 class="text-xl font-bold py-2">Diretoria</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 w-full">
          <div
            v-for="(doctor, index) in this.doctors.data.filter(
              (d) => d.attributes.field == 'Diretoria'
            )"
            :key="index"
          >
            <doctor-card :doctor="doctor" />
          </div>
        </div>
      </div>
      <div id="conselho-fiscal">
        <h3 class="text-xl font-bold py-2">Conselho Fiscal</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 w-full">
          <div
            v-for="(doctor, index) in this.doctors.data.filter(
              (d) => d.attributes.field == 'Conselho Fiscal'
            )"
            :key="index"
          >
            <doctor-card :doctor="doctor" />
          </div>
        </div>
      </div>
      <div id="responsavel">
        <h3 class="text-xl font-bold py-2">
          Apresentação do responsável atual pela Associação
        </h3>
        <div>
          <div
            class="
              flex flex-col
              sm:flex-row
              shadow
              bg-white
              rounded-lg
              h-2/3
              md:h-48
              m-2
            "
          >
            <img
              class="object-cover w-1/3 mx-auto"
              src="https://res.cloudinary.com/ame-rio/image/upload/v1650556493/americo-em-portugal.jpg"
              alt="Profile"
            />
            <p
              class="
                text-base text-justify text-gray-600
                m-auto
                px-5
                py-2
                overflow-y-auto
              "
            >
              Américo Domingos Nunes Filho é escritor, orador e pesquisador
              espírita, radicado na cidade do Rio de Janeiro, fundador e
              vice-presidente da ADE-RJ (Associação de Divulgadores do
              Espiritismo do Rio de Janeiro), fundador e presidente da AME-RIO
              (Associação Médico-Espírita do Rio de Janeiro) e sócio-honorário
              da AME PORTO - Associação Médico-Espírita da Área Metropolitana do
              Porto. <br />
              Formado em Medicina, pela Escola de Medicina e Cirurgia da
              UNI-RIO, exercendo a especialidade da Pediatria.
            </p>
          </div>
        </div>
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
export default {
  components: { DoctorCard, BookCard },
  data() {
    return {
      doctors: {},
      books: {},
    }
  },
  async fetch() {
    this.doctors = await this.$axios.$get('/api/doctors')
    this.books = await this.$axios.$get('/api/books?populate=*')
  },
  fetchOnServer: true,
}
</script>
