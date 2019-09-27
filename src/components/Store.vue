<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col bg-dark text-white">
                <a class="navbar-brand">SPORTS STORE</a>
                <cart-summary />
            </div>
        </div>
        <div class="row">
            <div class="col-3 bg-info p-2">
                <category-controls class="mb-5" />
                <button class="btn btn-block btn-warning mt-5"
                        v-on:click="setShowSearch(true)">
                    Search
                </button>
            </div>
            <div class="col-9 p-2">
                <search />
                <product-list />
            </div>
        </div>
    </div>
</template>

<script>
    import ProductList from "@/components/ProductList";
    import CategoryControls from "@/components/CategoryControls";
    import CartSummary from "@/components/CartSummary";
    import Search from "@/components/Search";
    import {mapMutations} from "vuex";

    export default {
        name: "Store",
        components: {Search, CartSummary, CategoryControls, ProductList},
        methods: {
            ...mapMutations(["setShowSearch"])
        }
    }
</script>

<style scoped>

</style>
