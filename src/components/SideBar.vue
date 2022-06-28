<template>
    <aside>
        <div class="logo">
            <img src="../assets/logo.png" alt="vue" srcset="">
        </div>
    </aside>
</template>
<script setup>
// export default {
//     setup() {
        
//     },
// }
</script>
<style lang="scss" scoped>
aside{
    display: flex;
    flex-direction: column;
    // width: var(--sidebar-width);
    width: calc(2rem + 32px);
    min-height: 100vh;
    overflow: hidden;
    padding: 1rem;

    background: var(--dark);
    color: var(--light);

    transition: 0.2s ease-out;

    @media(max-width: 768px) {
        position: fixed;
        z-index: 99;
    }
}

</style>