<template>
  <nav class="hidden lg:flex space-x-10">
    <DesktopHeaderLink
      v-for="navLink in navLinks"
      :key="navLink.title"
      :link="navLink.route"
      :text="navLink.title"
    />
  </nav>
</template>

<script>
export default {
  data: () => {
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