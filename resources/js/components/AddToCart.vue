<template>
    <div class="container">
        <hr />
        <button
            class="btn btn-medium btn-buy"
            style="
                background-color: black;
                color: white;
                font-size: 14px;
                text-transform: uppercase;
            "
            @click.prevent="addProductToCart()"
        >
            Thêm vào giỏ
        </button>
    </div>
</template>
<script>
export default {
    data(){

    },
    props:['productId','userId'],
    methods:{
        addProductToCart(){
            if(this.userId==0){
                this.$toastr.e('Bạn cần đăng nhập để thực hiện hành động này!!!');
                return;
            }
        }
    }
};
</script>
