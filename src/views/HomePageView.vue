<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();

const goToNextPage = () => {
    router.push('/khoa-hoc');
};

</script>

<template>
    <div class="ContentTitle">
        <h3>ABOUT US</h3>
    </div>
    <p class="ContentBody">
        The English Hub là dự án được tạo ra nhằm cải thiện kỹ năng tự học và nâng cao nhận thức ngôn ngữ trong
        học tập/công việc của mọi người ở mọi độ tuổi với sự can thiệp của trí tuệ nhân tạo và công nghệ cá nhân
        hoá được thiết kế riêng cho từng học sinh
        <br />-Sứ mệnh: Đưa ra các kỹ năng cần thiết về đời sống, đặc biệt là tự học song song với Tiếng Anh
        nhằm tạo ra thế hệ trẻ có khả năng tự phát triển trong tương lai.
        <br />-Tầm nhìn: Tạo ra một hệ sinh thái giúp học viên ở mọi độ tuổi có thể tự xử lý tất cả các chứng
        chỉ Tiếng Anh
        <br />-Chiến lược: Lộ trình cá nhân hoá theo tuần và AI giúp học sinh luyện tập ngôn ngữ song song với
        tạo thói quen tự học, tự xử lý vấn đề trong các môi trường khác nhau.
        <br />The English Hub được tạo ra với mục đích giải quyết việc thiếu hụt các kỹ năng sống cần thiết, đặc
        biệt là tự học và vận dụng Tiếng Anh trong môi trường học và làm tại Việt Nam. Với sự can thiệp của công
        nghệ và trí tuệ nhân tạo trong lĩnh vực giáo dục, chúng tôi tạo ra một lộ trình cá nhân hoá theo tuần
        nhằm giúp học viên luyện tập phản xạ ngôn ngữ song song với tạo thói quen tự học và tự xử lý vấn đề xã
        hội.

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