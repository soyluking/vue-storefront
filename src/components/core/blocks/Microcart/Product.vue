<template>
  <div>
    Core product row
  </div>
</template>

<script>
import AddToCart from 'src/components/core/AddToCart.vue'
import { thumbnail } from 'src/lib/filters'

export default {
  name: 'Product',
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  computed: {
    thumbnail () {
      return thumbnail(this.product.image, 150, 150)
    }
  },
  components: {
    AddToCart
  }
}
</script>
