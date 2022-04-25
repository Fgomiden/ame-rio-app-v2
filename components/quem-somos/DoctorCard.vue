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
      <!-- <img
        class="object-cover w-1/3"
        src="https://upload.wikimedia.org/wikipedia/commons/7/7c/Profile_avatar_placeholder_large.png"
        alt="Flower and sky"
      /> -->

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