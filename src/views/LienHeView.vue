<script lang="ts">
import { defineComponent, ref } from 'vue';
import axios from 'axios';

export default defineComponent({
    setup() {
        const formData = {
            name: ref(''),
            email: ref(''),
            phone: ref(''),
            facebook: ref(''),
        };

        const submitForm = async () => {
            try {
                const response = await axios.post('http://localhost:3000/api/leads', {
                    name: formData.name.value,
                    email: formData.email.value,
                    phone: formData.phone.value,
                    facebook: formData.facebook.value,
                });

                // Xử lý phản hồi thành công từ backend
                console.log(response);
                console.log('Lead submitted successfully:', response.data);
            } catch (error) {
                // Xử lý lỗi nếu có
                console.error(error);
                console.error('Error submitting lead:', error);
            }
        };

        return { formData, submitForm };
    },
});
</script>

<template>
    <div class="ContentTitle">
        <h3>LIÊN HỆ</h3>
    </div>
    <div class="ContentBody">
        <form @submit.prevent="submitForm">
            <div>
                <label for="name">Họ tên</label>
                <input type="text" id="name" v-model="formData.name.value" required>
            </div>
            <div>
                <label for="email">Email</label>
                <input type="email" id="email" v-model="formData.email.value" required>
            </div>
            <div>
                <label for="phone">Số điện thoại</label>
                <input type="tel" id="phone" v-model="formData.phone.value" required>
            </div>
            <div>
                <label for="facebook">Link Facebook</label>
                <input type="url" id="facebook" v-model="formData.facebook.value">
            </div>
            <button type="submit">Gửi</button>
        </form>
    </div>
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
    /* text-align: justify */
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

form input {
    padding: 15px;
    border: 1px solid #ccc;
    border-radius: 3px;
    margin-bottom: 10px;
    width: 100%;
    box-sizing: border-box;
    color: #2C3E50;
    font-size: 13px;
}

form button {
    width: 100px;
    background: #0003ca;
    font-weight: bold;
    color: white;
    border: 0 none;
    border-radius: 1px;
    cursor: pointer;
    padding: 10px;
    margin: 10px 5px;
    text-decoration: none;
    font-size: 14px;
}
</style>
