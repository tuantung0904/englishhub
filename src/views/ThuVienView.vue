<script setup lang="ts">
</script>

<template>
    <div class="ContentTitle">
        <h3>THƯ VIỆN</h3>
    </div>
    <p class="ContentBody">
        Chưa có dữ liệu
    </p>
    <button class="ContentCTA">
        <span class="ContentCTAText">SWIPE</span>
        <img class="ContentCTAArrow" src="/src/assets/images/arrow.png" />
    </button>
</template>

<style scoped>
.ContentLeft .ContentTitle {
    position: relative;
    display: flex;
    align-items: center;
    margin-bottom: 15px
}

.ContentLeft .ContentTitle h3 {
    font-size: 42px
}

.ContentLeft .ContentTitle:before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 35%;
    height: 5px;
    background-color: #e2ab2d
}

.ContentLeft .ContentTitle:after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 30px;
    width: 30px;
    height: 5px;
    background-color: #0003ca
}

.ContentLeft .ContentBody {
    font-size: 16px;
    text-align: justify
}

.ContentLeft .ContentCTA {
    border-radius: 10px;
    border: 2px solid #E2AB2D;
    background-color: transparent;
    margin-top: 15px;
    width: 170px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    align-self: flex-end;
    text-align: left;
    position: relative;
    cursor: pointer
}

.ContentLeft .ContentCTA .ContentCTAArrow {
    position: absolute;
    top: 50%;
    right: 10px;
    transform: translateY(-50%);
    width: 80px;
    height: 20px
}

.ContentLeft .ContentCTA .ContentCTAText {
    margin-right: 80px;
    margin-top: 5px
}
</style>
