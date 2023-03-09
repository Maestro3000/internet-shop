<template>
    <div class="ideas">
        <HeroInformation
        title="It started with a small idea"
        descrption="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
        colorTitle="#fff"
        colorDescription="#fff"
        colorLink="#fff"
        background="var(--black)"/>
        <img src="/img/room.jpg" alt="room">
    </div>
</template>

<script setup>
import HeroInformation from '@/components/Hero-information.vue'
</script>

<style lang="scss" scoped>
.ideas{
    padding: 0 80px;
    margin-bottom: 60px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 16px;
}
</style>