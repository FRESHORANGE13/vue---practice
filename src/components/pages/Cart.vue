<script>
import CartItem from "../widgets/CartItem.vue";

export default{
    data(){

        return{
            cartItems: [
             {
                imgURL : "https://m.media-amazon.com/images/I/61c2WmfHfvL._AC_.jpg",
                name: "Nemo socks",
                description: "socks with 2 toe areas that are shaped like Nemo",
                price: "$200.00",
                inCart: false
            },
            {
                imgURL : "https://m.media-amazon.com/images/I/41kwCyt8qyL._AC_SX679_.jpg",
                name: "Goose socks",
                description: "socks with a hyper-realistic goose design",
                price: "$199.99",
                inCart: false
            },
            {
                imgURL : "https://cdn.media.amplience.net/s/hottopic/20980202_hi?$productMainDesktopRetina$&fmt=auto",
                name: "Shrek socks",
                description: "premium quality shrek socks for shrek fans only",
                price: "$5.8763",
                inCart: false
            },
            {
                imgURL : "https://ooohyeah.com/cdn/shop/files/GWS23802_1.jpg?v=1705358432&width=880",
                name: "FLUFFY COW SOCKS :)))))",
                description: "THE BEST SOCKS IN THE ENTIRE WORLD",
                price: "$7235897Y109834.99",
                inCart: false
            }], 
            myCart: []
        }
    },
    
    components: {
        CartItem
    },
   
    methods: {
        select(option) {
            this.myCart.push(option);
            console.log(this.myCart)
        }
    }

}

</script>
<template>
    <header class="CartList">
        <h1> Items</h1>
    </header>

    <div class="layout">
        <div class="shoppingCartGrid">
            <CartItem v-for="cartI in cartItems" :cartItem="cartI" :key="cartI.name" v-on:click="select(cartI)" />

        </div>
    </div>
    
    <header class="ShoppingCart"> 
        <h1> Your Shopping Cart </h1> 
    </header>
    
    <div class="shoppingCartGrid">
        <CartItem v-for="item in myCart" :cartItem ="item" :key="item.name" />
    </div>
</template>

<style>
.ShoppingCart{
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    margin: 0px 30px;
}
.shoppingCartGrid {
    margin-top: 48px;
    padding: 0px 30px;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 40px 24px;
    -webkit-box-align: start;
    align-items: start;
}
</style>