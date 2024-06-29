<template>
  <div>
    <div
      class="
        flex flex-col
        sm:flex-row
        shadow
        h-28
        bg-white
        rounded-lg
        m-2
      "
    >
      <div class="p-2">
        <h3 class="text-base font-medium text-gray-800">
          {{ doctor.name }}
        </h3>
        <h3 class="text-base text-gray-600 pt-2">
          {{ doctor.role }}
        </h3>
        <h3 class="text-base text-gray-600">
          {{ doctor.profession }}
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