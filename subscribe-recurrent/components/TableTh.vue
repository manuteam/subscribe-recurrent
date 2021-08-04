<script>
export default {
  name: "TableTh",
  render: function (createElement) {
    return createElement(
      'th', {
        style: {
          minWidth: this.width + 'px'
        },
        class: {
          pl7: this.className
        },
      },
      this.$slots.default
    )
  },
  props: {
    width: {
      type: Number,
      required: true
    },
    className: {
      type: Boolean,
      required: false
    }
  }
}
</script>

<style scoped>

</style>
