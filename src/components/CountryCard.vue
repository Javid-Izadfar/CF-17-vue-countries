
<template>
    <li>
        <div class="country-img">
            <img name="flag" class="flag" :src="flag" alt="flags">
        </div>
        <div class="name-like">
            <h2 v-if="title" class="title">
                {{ title }}
            </h2>
            <input type="image" class="like" src="src/assets/svg/fi-rs-heart.svg">
        </div>
        <div>
            <p v-if="desc" class="desc">
                {{ desc }}
            </p>
        </div>
        <button class="button" href="#">
            <span class="more">Learn more </span>
            <img class="arrow" src="src/assets/svg/arrow.svg">
        </button>
    </li>
</template>

<script setup>
// import { string, number } from 'vue-types'
import { defineProps } from 'vue'

const props = defineProps({
    title: {
        type: String,
        default: 'country-name'
    },
    desc: {
        type: String,
        default: 'country-information'

    },
    flag: {
        type: String,
        default: 'flag-image'

    }
})

// export default {
//     data() {
//         return {
//             imageSrc: 'src/assets/svg/fi-rs-heart.svg',
//             clickedImageSrc: 'src/assets/svg/red-heart.svg'
//         }
//     },
//     methods: {
//         changeImage() {
//             this.imageSrc = this.clickedImageSrc;
//         }
//     }
// }

// document.getElementById("heart-button").onClick = function () {
//     if (this.src.match("src/assets/svg/fi-rs-heart.svg")) {
//         this.src = "src/assets/svg/red-heart.svg";
//     } else {
//         this.src = "src/assets/svg/fi-rs-heart.svg"
//     }
// }

</script>

<style scoped>
li {
    height: 412px;
    flex-basis: 23%;
    /* width: 25%; */
    /* padding: 15px; */
    background-color: rgba(225, 225, 225, 0.5);
    margin-top: 30px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    /* justify-content: space-around; */
    align-items: center;
}

.flag {
    width: 267.5px;
    height: 150px;
    flex-basis: calc(150/412);
    /* height: calc(150/412); */
    border-radius: 5px;
    margin-top: 19px;
}

.name-like {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    flex-basis: calc(36/412);
    /* gap: 5px; */
    /* height: calc(36/412); */
}



.title {
    font-family: Inter;
    font-size: 16px;
    font-weight: 700;
    color: black;

}

.like {
    width: 36px;
    height: 36px;
    padding: 8px;
    background-color: white;
    border-radius: 36px;


}

.desc {
    font-family: Inter;
    font-size: 14px;
    font-weight: 400;
    flex-basis: calc(100/412);
    margin-top: 10px;
    padding: 0 20px;
    height: 100px;
    color: rgba(0, 0, 0, 0.7);
    /* height: calc(100/412); */
}

.button {
    flex-basis: calc(36/412);
    /* height: calc(36/412); */
    margin-top: 20px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 5px;
    margin-right: 160px;
    border-radius: 8px;
    background-color: white;
    border: none;
    padding: 8px 16px;

}

.more {
    font-family: Inter;
    font-size: 14px;
    font-weight: 500;
    color: black;


}
</style>