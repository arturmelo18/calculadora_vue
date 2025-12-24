<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="calculator-bg">
        <div class="calculator">
            <div class="calculator-screen"></div>
            <div class="calculator-keyboard">
                <div class="calculator-key"
                    v-for="key, index in state.keys"
                    :key="index"
                >
                {{ key }}
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { reactive } from 'vue';


const state = reactive({
    keys: ['0','1','2','3','4','5','6','7','8','9', '+', '-', '/', 'x', '=']
})

</script>

<style lang="css" scoped>

@import url('https://fonts.googleapis.com/css2?family=BBH+Hegarty&family=Nunito:ital,wght@0,200..1000;1,200..1000&display=swap');

.calculator-bg {
    background: #747171;
    margin: 50px auto;
    width: 400px;
    height: 650px;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.calculator {
    width: 400px;
    height: 550px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;    
    flex-direction: column;
}

.calculator-screen {
    border-radius: 10px;
    background: #aceee5;
    height: 100px;
    width: 350px;
}

.calculator-keyboard {
    margin-top: 50px;
    height: 390px;
    width: 350px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.calculator-key {
    background: #0bc08a;
    text-align: center;
    align-content: center;
    margin: 20px 20px;
    flex: 1 1 50px;
}
</style>

<style lang="css">
* {
    font-family: "Nunito", sans-serif;
    font-weight: bold;
}
</style>