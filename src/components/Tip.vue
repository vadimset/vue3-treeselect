<script>
  export default {
    name: 'vue-treeselect--tip',

    props: {
      type: {
        type: String,
        required: true,
      },
      icon: {
        type: String,
        required: true,
      },
    },

    render(slots) {
      const { type,icon } = this

      return (
        <div class={`vue-treeselect__tip vue-treeselect__${type}-tip`}>
          <div class="vue-treeselect__icon-container">
            <span class={`vue-treeselect__icon-${icon}`} />
          </div>
          <span class={`vue-treeselect__tip-text vue-treeselect__${type}-tip-text`}>
            {slots.default}
          </span>
        </div>
      )
    },
  }
</script>
