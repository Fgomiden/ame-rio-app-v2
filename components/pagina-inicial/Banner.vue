<template>
  <div class="flex flex-col md:flex-row">
    <div
      class="mx-auto md:flex-1 bg-stonehenge h-80 w-4/6 bg-no-repeat bg-cover"
    ></div>
    <div class="md:flex-1 mx-auto my-auto px-5">
      <h1
        class="
          text-left text-2xl
          md:text-4xl
          tracking-tight
          font-extrabold
          text-gray-900
        "
      >
        <span class="block">Associação Médico-Espírita</span>
        <span class="block">do Estado do Rio de Janeiro</span>
      </h1>
      <p
        class="
          mt-3
          text-base text-gray-500
          sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto
          md:mt-5 md:text-xl
          lg:mx-0
        "
      >
        Instituição que congrega os profissionais de saúde espíritas, cuja
        diretoria é composta por médicos.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Banner',
}
</script>

<style>
.bg-stonehenge {
  background-image: url('https://res.cloudinary.com/ame-rio/image/upload/v1653759158/Banner_Ame_Rio.png');
}
</style>