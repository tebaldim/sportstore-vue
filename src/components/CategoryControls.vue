<template>
    <div class="container-fluid">
        <div class="row my-2" v-for="c in categories" v-bind:key="c">
            <button class="btn btn-block"
                    v-on:click="setCurrentCategory(c)"
                    v-bind:class="c === currentCategory ? 'btn-primary' : 'btn-secondary'">
                {{ c }}
            </button>
        </div>
    </div>
</template>

<script>
    import {mapGetters, mapActions, mapState} from "vuex";

    export default {
        name: "CategoryControls",
        computed: {
            ...mapState(["currentCategory"]),
            ...mapGetters(["categories"])
        },
        methods: {
            ...mapActions(["setCurrentCategory"])
        }
    }
</script>

<style scoped>

</style>
