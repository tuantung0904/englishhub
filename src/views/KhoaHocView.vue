<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();

const goToNextPage = () => {
    router.push('/trai-nghiem');
};

</script>
<template>
    <div class="ContentTitle">
        <h3>LỘ TRÌNH HỌC</h3>
    </div>
    <p class="ContentBody">
        Alpha Hub: 15 sessions
        <br />Beta Hub: 20 sessions
        <br />Gamma Hub: 25 sessions
        <br />“Giỏi Tiếng Anh không đồng nghĩa với IELTS cao”
        <br />
        <br /> 1. Alpha Hub
        <br />Học các kỹ năng nền tảng cho 4 kỹ năng của IELTS
        <br />Làm quen với các hoạt động tự học ở level mới bắt đầu
        <br />Làm quen với các họạt động cộng đồng ở level Alpha - Làm quen - bài tập nhóm - quay video
        <br />
        <br />2. Beta Hub
        <br />Tham gia các buổi thuyết trình - nâng cấp kỹ năng tự học và các kỹ thuật trong IELTS.
        <br />tham gia các buổi book club - mini game hàng tuần với sự th ở Beta hub.
        <br />được ôn tập với AI ở 4 kỹ năng.
        <br />
        <br />3. Gamma Hub
        <br />Hoàn thiện kỹ năng và luyện đề ở cấp độ thi
        <br />Thi thử không giới hạn
        <br />Ôn tập với AI ở 4 kỹ năng
        <br />Tham gia các hoạt động cộng đồng với người nước ngoài
        <br />Tham gia các hoạt động ở hub với GV nước ngoài.
    </p>
    <button class="ContentCTA" @click="goToNextPage">
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
    text-align: justify;
    height: 300px;
    overflow-y: scroll;
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
