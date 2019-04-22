<template>
    <div>
        <h1>{{ msg }}</h1><hr>
        <h3>{{$store.state.count}}-{{count}}</h3>
        <div>
            <button @click="$store.commit('add')">+</button>
            <button @click="$store.commit('reduce')">-</button>
        </div>
    </div>
</template>
<script>
    import store from '@/vuex/store';
    import {mapState} from 'vuex';
    export default {
        data(){
            return {
                msg:'hello vuex'
            }
        },
        computed:{
            count(){
                return this.$store.state.count;
            }
        },
        store
    }
</script>