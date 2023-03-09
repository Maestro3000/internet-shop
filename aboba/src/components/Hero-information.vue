<template>
    <div class="hero-info" :style="{backgroundColor: background}">
        <div class="hero-info__text">
            <h2 class="hero-info__title" 
            :style="{color: colorTitle}">{{ title }}</h2>
            <span class="hero-info__description"
            :style="{color: colorDescription}">{{ descrption }}</span>
        </div>
        <ui-button background="rgba(249, 249, 249, 0.15)" type="link" to="/">
            View collection
        </ui-button>
        <!-- <a 
        :href="link" 
        :style="{color: colorLink}"
        class="hero-info-link">View collection</a> -->
    </div>
</template>

<script setup>
import uiButton from '@/components/UI/Button.vue'

const props = defineProps({
    title:{
        type: String,
        required: false,
    },
    descrption:{
        type: String,
        required: false,
    },
    link:{
        type: String,
        required: false,
    },
    colorTitle:{
        type: String,
        default: ""
    },
    colorDescription:{
        type: String,
        default: "#5B5676"
    },
    colorLink:{
        type: String,
        default: "#2A254B"
    },
    background:{
        type: String,
        default: "#fff"
    }  
})

</script>

<style lang="scss" scoped>
.hero{
    &-info{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
        background: #fff;
        max-width: 630px;
        padding: 50px 55px;
        min-height: 444px;
        &__title{
            font-family: var(--Clash);
            font-weight: 400;
            line-height: 1.5;
            margin: 0 0 20px 0;
        }
        &__description{
            color: var(--lightGray);
            font-size: 18px;
        }
    }
}
</style>