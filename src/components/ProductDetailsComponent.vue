<template>
    <div>
        <h3>Название продукта:{{ this.product.name }}</h3>
        <p>Цена продукта:{{ formattedPrice}}</p>
        <p v-if="product.available">Доступность товара: Available</p>
        <p v-else>Доступность товара: Out of stock</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                product:{
                    name:'Гель для душа',
                    price:99.99,
                    available:true,
                },
            };
        },
        computed:{
            formattedPrice(){
                return '$'+this.product.price;
            },
        },    
            
    };
</script>

<style lang="scss" scoped>

</style>