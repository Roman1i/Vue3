<template>
    <div>
        <p>name: {{ product.name }}</p>
        <p>price: {{ formattedPrice }}</p>
        <p>{{ isAvailable }}</p>
    </div>
</template>

<script>

export default {
  name: 'ProductDetails',

  data () {
    return {
      product: {
        name: 'ProductName',
        price: 10,
        available: false
      }
    }
  },

  computed: {
    formattedPrice () {
      return `$${this.product.price}`
    },

    isAvailable () {
      if (this.product.available) {
        return 'Available'
      } else {
        return 'Out of stock'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
