<template>
    <button 
    v-if="type === 'button'" 
    class="btn" 
    :style="{backgroundColor: background}">
        <slot/>
    </button>
    <router-link 
    v-else 
    :to="to" 
    class="btn" 
    :style="{backgroundColor: background}">
        <slot/>
    </router-link>
</template>

<script setup>

const props = defineProps({
    background:{
        type: String,
        required:false,
    },
    type:{
        type: String,
        default:'button',
    },
    to:{
        typeof: String,
        required:false,
    },
});

</script>


<style lang="scss" scoped>
.btn{
    background: var(--black);
    color: #fff;
    padding: 0 32px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    border: none;
    font-size: 16px;
    height: 56px;
    text-decoration: none;
    &:hover{
        opacity: .8;
    }
}
</style>