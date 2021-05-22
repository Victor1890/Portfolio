<template>
      <section id="hero" :style="banner.photo">
        <div class="hero-container">
            <h1>{{banner.name}}</h1>
            <h2>{{banner.aboutMe}}</h2>
            <a href="#about" class="btn-scroll scrollto" title="Scroll Down"><i class="bx bx-chevron-down"></i></a>
        </div>
    </section>
</template>

<script>

export default {
name: 'Banner',
props:['banner']
}
</script>
