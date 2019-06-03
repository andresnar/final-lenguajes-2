<template>
  <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade"
      transition="fade"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'http://boletinaldia.sld.cu/aldia/files/2017/12/demencia2.jpg'
          },
          {
            src: 'https://www.grupociudadjardin.com/wp-content/uploads/2018/11/señales-del-alzheimer-1200x600.jpg'
          },
          {
            src: 'https://www.infobae.com/new-resizer/VUKdcRin38pdK9Yeuj1EkS8o1Xs=/750x0/filters:quality(100)/s3.amazonaws.com/arc-wordpress-client-uploads/infobae-wp/wp-content/uploads/2017/09/20152401/Alzheimer-nota-infobae.jpg'
          }
        ]
      }
    }
  }
</script>

<style lang="stylus">
  #example-custom-transition
    .fade
      &-enter-active, &-leave-active, &-leave-to
        transition: .2s ease-out
        position: absolute
        top: 0
        left: 0

      &-enter, &-leave, &-leave-to
        opacity: 0
</style>