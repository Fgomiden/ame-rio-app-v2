<template>
  <div>
    <div
      class="
        flex flex-col
        sm:flex-row
        shadow
        h-24
        bg-white
        rounded-lg
        cursor-pointer
        m-2
      "
    >
      <div class="px-2">
        <h3 class="text-base font-medium text-gray-800">
          {{ doctor.attributes.name }}
        </h3>
        <h3 class="text-base text-gray-600 pt-2">
          {{ doctor.attributes.role }}
        </h3>
        <h3 class="text-base text-gray-600">
          {{ doctor.attributes.profession }}
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DoctorCard',
  props: {
    doctor: Object,
  },
}
</script>

<style>
</style>