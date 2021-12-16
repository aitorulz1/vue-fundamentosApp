<template>
    <h2>Counter</h2>

    <p> {{counter}} <sup>2</sup> = {{ getSquareValue() }}</p>

    <button @click="increaseCouter">+1</button>
    <button @click="decreaseCounter">-1</button>

</template>

<script>

export default {
    name: 'Counter',

    data() {
        return {
            counter: 6
        }
    },
    methods: {
        getSquareValue() {
            return this.counter * this.counter 
        },
        increaseCouter() {
            this.counter ++
        },
        decreaseCounter() {
            this.counter--
        }
    },
    computed: {
        squareCounted() {
            return this.counter * this.counter
        }
    }
}
</script>

<style>
    button{
        background-color: aquamarine;
        border-radius: 3px;
        color:#000;    
        cursor: pointer;
        transition: 0.3s ease-in-out;
        margin: 0 5px;
        padding: 5px 15px;
    }

    button:hiver {
        background-color:rgb(100, 177, 151);         
    }
</style>
