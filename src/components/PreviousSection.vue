<template lang="jade">

  a.previous-section(v-bind:style="styles" v-on:click.prevent.stop="scrollTo(href)"): i.fa.fa-angle-up.fa-2x

</template>

<style lang="stylus">

  @require '../assets/styles/mixins'

  .previous-section
    text-align center
    display block
    color #fff
    opacity 0.5
    padding 1em
    transition-all()

    &:hover
      opacity 1

</style>

<script lang="coffee">

  module.exports =
    methods:
      scrollTo: (selector) ->
        this.$dispatch 'scroll-to-element', selector

    props: [
      'href'
      'styles'
    ]

</script>

