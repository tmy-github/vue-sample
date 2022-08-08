<script setup lang="ts">
const itemName1: string = "Curry and Rice";
const itemName2: string = "Bike";

const price1: Number = 400;
const price2: Number = 40000;

const url1: string = "https://www.amazon.co.jp/dp/B08NG49Z7B/ref=redir_mobile_desktop?_encoding=UTF8&aaxitk=d884d81ffe140030fd580e1245e0f714&content-id=amzn1.sym.0eee0996-ff3e-4e55-9145-2933276c6b40%3Aamzn1.sym.0eee0996-ff3e-4e55-9145-2933276c6b40&hsa_cr_id=4598403530403&pd_rd_plhdr=t&pd_rd_r=a2c111d2-26e7-40d4-8047-992c06e57a97&pd_rd_w=z1jk6&pd_rd_wg=dQaEB&qid=1659957912&ref_=sbx_be_s_sparkle_lsi4d_asin_0_img&sr=1-1-b80f50f1-2970-4daf-ab14-5b4b5496c56c";

const buy = (itemName: string) => {
    alert("Are you sure to buy " + itemName + "?");
};

const input = () => {
    console.log("Inputting...");
};
</script>

<template>
    <div class="container">
        <h1>Payment</h1>
        <input v-on:input="input" />
        <div class="payment">
            <label>{{ itemName1 }}</label>
            <label>{{ price1 }} yen</label>
            <a v-bind:href="url1">Bought at ...</a>
            <button v-on:click="buy(itemName1)">Buy</button>
        </div>
        <div class="payment">
            <label>{{ itemName2 }}</label>
            <label>{{ price2 }} yen</label>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.payment {
    display: flex;
    justify-content: space-between;
    height: 80px;
    width: 400px;
    background-color: orange;
    align-items: center;
    margin-bottom: 10px;
}

label {
    font-size: 20px;
    font-weight: bold;
}
</style>