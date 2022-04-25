<template>
  <nav class="grid gap-y-8">
    <NuxtLink
      v-for="navLink in navLinks"
      :key="navLink.title"
      :to="navLink.route"
      class="
        -m-3
        p-3
        flex
        items-center
        justify-center
        space-x-3
        rounded-md
        hover:bg-gray-50
        transition
        ease-in-out
        duration-150
      "
    >
      <div
        class="text-base leading-6 font-medium text-gray-900 dark:text-white"
      >
        {{ navLink.title }}
      </div>
    </NuxtLink>
  </nav>
</template>

<script>
export default {
  data: function () {
    return {
      navLinks: [
        {
          title: 'Quem Somos',
          route: '/quem-somos',
        },
        {
          title: 'História',
          route: '/historia',
        },
        {
          title: 'Patrono',
          route: '/patrono',
        },
        {
          title: 'Artigos',
          route: '/posts',
        },
      ],
    }
  },
}
</script>