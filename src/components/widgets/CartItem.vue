<script>
export default{
    props: {
        cartItem:{
            imgURL: String,
            name: String,
            description: String,
            price: String,
            inCart: Boolean
        }
        
    }
   
}

//CHANGE THE TEMPLATE STUFF!!  
</script>
<template>
    <div class="cart-item">
            <div class="cart-item__image">
                <img :src= "cartItem.imgURL" alt="news image" />
            </div>
            <div class="cart-item__content">
                <h3 class="cart-item__title">{{ cartItem.name }}</h3>
                <h3 class="cart-item__price">{{ cartItem.price }}</h3>
                <p class="cart-item__decription">{{ cartItem.description}}</p>
            </div>
    </div>
</template>

<style>
.cart-item {
    border-bottom: 1px solid var(--color-border);
    padding: 16px;
}
.cart-item__image {
    /* margin-right: 16px; */
    width: 100%;
    height: 100%;
    height: 200px;
}

.cart-item__image>img {
    object-fit: cover;
    overflow: hidden;
    height: 100%;
    width: 100%;
}

.cart-item__content {
    display: flex;
    flex-flow: column;
    justify-content: space-between;
    gap: 16px;
}

.cart-item__description {
    height: 70px;
    padding-top: 0px;
    line-height: 24px;
    overflow: hidden;
    text-overflow: ellipsis;
    font-size: 10px;
}
</style>

