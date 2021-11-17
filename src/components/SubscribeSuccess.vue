<template>
    <div class="container-subscribe">
        <div class="image-notifi">
            <img src="../assets/success.png" alt="">
            <h3>Đăng ký thành công</h3>
        </div>
        <div class="content-notifi">
            <p>Bạn đã đăng ký thành công khóa học trên Study-arts.
            Chúng tôi sẽ gửi mail cung cấp thông tin đăng nhập cho bạn ngay sau khi
            kiểm tra được thông tin chuyển khoản.</p>
            <p>Bạn hãy lưu lại mã chuyển khoản (nội dung chuyến khoản) đế có thể quản lý
thông tin sau này
</p>
        </div>
        <div class="button-back">
            <a href="">Quay lại trang khóa học</a>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Subscribe',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .container-subscribe{
        padding: 40px 0px;
    }
    .image-notifi img{
        width: 100px;
        height: 100px;
        display: block;
        margin:0px auto;
    }
    .image-notifi h3{
        text-align: center;
        color: #444444;
    }
    .content-notifi{
        display: block;
        margin:70px auto;  
        width: 60%;
    }
    .content-notifi p{
        text-align: center;
        line-height: 24px;
    }
    .button-back a{
        text-decoration: none;
        background-color: #0071c5;
        color: #fff;
        font-size: 18px;
        padding: 10px 20px;
        border-radius: 5px;
        text-align: center;
        display: block;
        margin: 0px auto;
        width: 30%;
    }
    @media screen and (max-width: 600px) {
    .content-notifi{
        display: block;
        margin:50px 10px;  
        width: 95%;
    }
    .button-back a{
        width: 70%;
    }
}
</style>