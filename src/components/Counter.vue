<template>
    <div class="counter">
        <h3>Counter : {{ number }}</h3>
        
        <div>
            <label for="counter" v-bind:title="number">Counter: </label>
            <input type="text" v-model="number">
            
            <button class="btn" v-on:click="increase">+</button>
            <button class="btn" v-on:click="decrease">-</button>
            <button class="btn" v-on:click="increase10">+10</button>
            <button class="btn" v-on:click="multiply">X2</button>
            

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
    
    .btn {
        background-color: black;
        color: white;
        width: 32px;
        border-radius: 4px;
        border: 2px solid grey;
        padding: 3px;
        margin: 2px;
        &:hover {
            color: black;
            background-color: white;
        }
    }
</style>>

