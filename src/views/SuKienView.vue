<script setup lang="ts">
</script>

<template>
    <div class="PageContent">
        <div class="ContentLeft">
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
            <button class="ContentCTA">
                <span class="ContentCTAText">SWIPE</span>
                <img class="ContentCTAArrow" src="/src/assets/images/arrow.png" />
            </button>
        </div>
        <div class="ContentRight">
            <img class="BigLogo" src="/src/assets/images/BigLogo-B8ylSlHo.png" />
            <img class="Sticker Sticker1" src="/src/assets/images/sticker1-B5DMJB1G.png" />
            <img class="Sticker Sticker2" src="/src/assets/images/sticker2-gGfY4Bd0.png" />
            <img class="Sticker Sticker3" src="/src/assets/images/sticker3-yUUXBlou.png" />
        </div>
    </div>
</template>

<style scoped>
.PageContent {
    flex-grow: 1;
    display: grid;
    grid-template-columns: 1fr 1fr;
    font-family: BDLifelessGrotesk
}

.ContentLeft {
    display: flex;
    flex-direction: column;
    margin-top: 15px;
    padding: 15px 30px;
    background-color: #fff;
    border-radius: 0 0 0 10px;
    border-right: 5px solid #E2AB2D;
    max-height: 100%;
    color: #8e8e8e
}

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

.ContentRight {
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px
}

.ContentRight .BigLogo {
    max-width: 100%
}

.ContentRight .Sticker {
    position: fixed;
    z-index: 99;
    max-width: 100%;
    max-height: 100%;
    display: block;
    margin: 0 auto
}

.ContentRight .Sticker1 {
    height: 75vh;
    bottom: 0;
    right: 1vw
}

.ContentRight .Sticker2 {
    height: 30vh;
    bottom: 0vh;
    left: 50vw
}

.ContentRight .Sticker3 {
    height: 22vh;
    bottom: 60vh;
    left: 40vw
}
</style>