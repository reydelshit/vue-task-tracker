<template>
    <button v-on:click="onClick()" :style="{ background: color}" class=" btn">{{text}}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    methods: {
        onClick(){
            console.log('hey brzother')
        },
    }
}
</script>