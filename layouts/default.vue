<template>
    <div>
        <NavBar />
        <nuxt />
        <!-- <Footer /> -->
    </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
export default {
    components: {
        NavBar
    },
}
</script>