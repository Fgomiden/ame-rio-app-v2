<template>
  <div class="relative bg-white overflow-hidden">
    <main class="flex flex-col flex-wrap mx-auto max-w-7xl px-4">
      <section id="banner">
        <banner />
      </section>
      <section id="principios">
        <div class="flex flex-col">
          <div class="flex flex-col md:flex-row md:justify-around">
            <principle-card
              title="Missão"
              description="Divulgar para os interessados em saúde a visão científica da medicina espiritual trazida pela doutrina espírita."
              image="./icons/globe-icon.svg"
            />
            <principle-card
              title="Visão"
              description="Ser uma entidade que promove e vincula à visão da comunidade
                  científica o espiritismo para o entendimento da Saúde."
              image="./icons/stethoscope-icon.svg"
            />
          </div>
          <div class="flex">
            <principle-card
              title="Valores"
              isValores
              image="./icons/doctor-icon.svg"
            />
          </div>
        </div>
      </section>
      <section id="atividades">
        <atividades />
      </section>
      <section id="fale-conosco">
        <contact-form />
      </section>
    </main>
  </div>
</template>

<script>
import Atividades from '~/components/pagina-inicial/Atividades.vue'
import Banner from '~/components/pagina-inicial/Banner.vue'
import ContactForm from '~/components/pagina-inicial/ContactForm.vue'
import PrincipleCard from '~/components/pagina-inicial/PrincipleCard.vue'
export default {
  components: { PrincipleCard, Banner, ContactForm, Atividades },
}
</script>
