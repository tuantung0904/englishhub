<script setup lang="ts">

</script>

<template>
    <div></div>
</template>



<style scoped>
.Navbar {
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    z-index: 99;
    border-bottom: 2px solid rgba(255, 255, 255, .6)
}

.Navbar .LogoDiv {
    margin: 20px
}

.Navbar .NavButtons {
    display: flex;
    justify-content: flex-start;
    align-items: center;
}

.Navbar .LoginButtonDiv {
    display: flex;
    justify-content: flex-end;
    align-items: center
}

.Navbar .nav-button {
    padding: 10px 20px;
    margin: 10px;
    background: #ffffff80;
    background: linear-gradient(90deg, #ffffffb3, #fff6);
    border: 1px solid rgba(255, 255, 255, .5);
    border-radius: 10px;
    font-weight: 300;
    font-size: 14px;
    color: #fff
}
</style>