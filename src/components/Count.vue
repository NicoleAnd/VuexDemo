<template>
    <div>
        <h1>{{ msg }}</h1><hr>
        <!-- <h3>{{$store.state.count}}-{{count}}</h3> -->
        <h3>{{count}}</h3>
        <div>
            <button @click="$store.commit('add',10)">+</button>
            <button @click="reduce">-</button>
        </div>
    </div>
</template>
<script>
    import store from '@/vuex/store';
    import {mapState,mapMutations} from 'vuex';
    export default {
        data(){
            return {
                msg:'hello vuex'
            }
        },
        // computed:{
        //     count(){
        //         return this.$store.state.count;
        //     }
        // },
        // computed:mapState({
        //     count: state=>state.count
        // }),
        computed: mapState(['count']),
        methods: mapMutations(['add','reduce']),
        store
    }
</script>