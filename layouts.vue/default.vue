<template>
    <div>
        <Nuxt />
    </div>
</template>


<script>
  export default {
    head: {
        title: 'Verify Account',
        titleTemplate: '%s | Patronize',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Home page description'
          }
        ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }],
      
    }
  }
</script>