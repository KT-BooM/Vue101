<template>
    <div class="counter">
        Counter : {{ number }}
        <div>
            <label for="counter" v-bind:title="number">Counter: </label>
            <input type="text" v-model="number">
            <button v-on:click="increase">+</button>
            <button v-on:click="decrease">-</button>
            <button v-on:click="increase10">+10</button>
            <button v-on:click="multiply">*2</button>

        </div>
        
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            number : 10,
        }
    },
    
    methods: {
        increase() {
            this.number++;
            console.log(this.number);
        },
        decrease() {
            this.number--;
        },
        increase10() {
            this.number+=10;
        },
        multiply() {
            this.number*=2;
        }
    }
}

</script>

<style lang="scss" scoped>

</style>>

