<template>
    <div class="card my-5">
        <div class="card-body">
            <h5 class="text-center card-title">
                {{ product.title }}
            </h5>
            <p class="text-center text-muted card-text display-4">
                $ {{ Number(product.price).toFixed() }}
            </p>
            <button :disabled="isInCart" v-on:click="$emit('add-to-cart', product)" class="btn btn-primary form-control">
                {{ isInCart ? 'Added to Cart' : 'Add to Cart' }}
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'product',
    props : ['product', 'isInCart']
};
</script>

