<template>
    <div>
        <NavBar />
        <slot />
    </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
// import Vue from "vue";
export default {
    components: {
        NavBar
    },
}
</script>