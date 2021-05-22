<template>
        <a class="nav-link scrollto" :href="href">{{title}}</a>
</template>

<script>
export default {
  props: {
  title: String,
  href: String
  },
  name: 'Navigation',
 data: function () {
    return {
     }
  },
}
</script>