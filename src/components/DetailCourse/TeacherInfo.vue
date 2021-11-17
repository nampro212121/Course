<template>
  <div class="container">
    <div class="flex-container">
        <div class="media-teacher">
            <div class="box-media">
                <img src="https://static2.yan.vn/YanNews/2167221/201704/20170428-104537-samsung-galaxy-j7-selfie_600x450.jpg"  alt="https://giuseart.com/wp-content/uploads/2017/10/Banner-Kh%C3%B3a-h%E1%BB%8Dc-Ti%E1%BA%BFng-Anh-3.jpg">
            </div>
            <div class="box-text">
                <p class="name-teacher">{{DetailCourse.teacher.userName}}</p>
                <p class="icon-student">👨‍🎓</p>
                <p class="number-student">{{DetailCourse.teacher.totalStudent}}{{}} học viên</p>               
            </div>
            <div class="valuate-teacher">
                <p>{{DetailCourse.courseEvaluate}}</p>
            </div>
        </div>
        <div class="detail_course">
            <h3>{{DetailCourse.courseName}}</h3>
            <p>
                {{DetailCourse.courseSynopsis }}
            </p>
        </div>
    </div>
    <div class="flex-container">
        <div class="media-course">
            <div class="box-media-course">
                <img :src="DetailCourse.courseCover"  alt="">
            </div>
        </div>
        <div class="detail_info-course">
            <div class="box-info">
                <span>
                    <button id="cart" href="" v-on:click="added(1,2,3,4)">Thêm vào giỏ hàng</button>
                    <button id="sub" href="" >Đăng kí khóa học</button>
                </span>
                <div class="price">
                    <h3>Học trọn gói với: </h3>
                    <div class="style-1">
                    <del>
                        <span class="amount">{{DetailCourse.coursePrice }} đồng</span>
                    </del>
                    <ins>
                        <span class="amount">{{DetailCourse.coursePriceDiscount }} đồng</span>
                    </ins>
                    </div>
                </div>
                <div class="info">
                    <p>Thời gian học dự kiến: <b>{{DetailCourse.courseEstimatedStudyTime}}</b></p>
                    <p>Giáo trình:</p>
                    <p>Thời hạn giảm giá:</p>
                    <p>Số học viên hiện tại:</p>
                </div>
            </div>
        </div>
    </div>
    <div class="content-course">
        <div class="header-tab">
            <h3>Nội dung khóa học<!--  -->
            <span><p v-on:click="Toggle('content')">&#128317;</p></span>
            </h3>
        </div>
        <div v-if="content" class="content">
        <p>AutoCAD - công cụ chỉnh sửa bản vẽ kỹ thuật đỉnh cao</p>
        <p>Việc học AutoCAD không còn xa lạ với dân kỹ thuật, dản kiến trúc, dân thiết kế, bất cứ ai làm những công việc liên quan đến bản vẽ kỹ thuật và xây dựng. Đây là phần mềm được sử dụng nhiều nhất vào xây dựng, thiết kế và chỉnh sửa các bản vẽ kỹ thuật cao như thiết kế kiến trúc nội thất - ngoại thất, quy hoạch, vẽ kỹ thuật cồng nghiệp, kỹ thuật dân dụng cơ sờ hạ tầng,...
        Và nếu bạn là:</p>
        <p>-	Học sinh mới tốt nghiệp THPT có đam mê thiết kế nội thất - ngoại thất, yêu thích công việc liên quan đến kỹ thuật, kiến trúc, xây dựng, muốn tự học AutoCAD tại nhà trước khi học cao hơn tiết kiệm chi phí</p>
        <p>-	Sinh viên, học viên các ngành kỹ thuật như Xây dựng, kiến trúc, công trình điện nước, cơ khí... mới vào học chuyên ngành, muốn học khóa học AutoCAD Online mới đế sớm làm quen với cỏng cụ này</p>
        <p>-	Sinh viên học viên chuấn bị ra trường, chuẩn bị đi làm tại các công ty, doanh nghiệp, muốn học đế trau dồi hơn kiến thức và kỹ năng sử dụng AutoCAD một cách thành thạo</p>
        <p>-	Nhân viên thiết kế, kỹ sư mới đi làm, muốn được dạy Autocad đế trau dồi hơn kỹ năng và tư duy công cụ AutoCAD thành thạo</p>

        </div>
    </div>
    <div class="catalog-course">
         <div class="header-tab">
            <h3>Mục lục khóa học<!--  -->
            <span><p v-on:click="Toggle('catalog')">&#128317;</p></span>
            </h3>
        </div>
        <div v-if="catalog" class="content">
        <h3><span>&#128160;</span>Bảng chữ cái trong tiếng Nhật<!--  --></h3>
        <table class="lesson_content">
            <tr>
                <td>➧Bài 1: Bảng chữ cái Hiragana</td>
                <td>Thời gian học dự kiến:<span>5:00</span></td>
            </tr>
            <tr>
                <td>➧Bài 2: Bảng chữ cái Katakana</td>
                <td>Thời gian học dự kiến:<span>5:00</span></td>
            </tr>
        </table>
        <h3><span>&#128160;</span>Chào hỏi cơ bản<!--  --></h3>
         <table class="lesson_content">
            <tr>
                <td>➧Bài 1: Chào hỏi xã hội</td>
                <td>Thời gian học dự kiến:<span>5:00</span></td>
            </tr>
            <tr>
                <td>➧Bài 2: Chào hỏi tại nơi làm việc</td>
                <td>Thời gian học dự kiến:<span>5:00</span></td>
            </tr>
        </table>
        </div>
    </div>
  </div>
   <div class="shopping-cart">
        <p class="button-icon" v-on:click="OpenModal()"><img src="./shopping-icon.png" alt=""><b class="total-item-cart">3</b></p>
        <!-- The Modal -->
        <div id="myModal-Cart" class="modal">

            <!-- Modal content -->
            <div class="modal-content">
                <span v-on:click="CloseModal()" class="close">&times;</span>
                <div class="cart-content">
                    <table class="cart-table" style="width:100%;">
                    <tr id="item-course" >
                        <td class="item-image" >
                            <img class="" src="https://giuseart.com/wp-content/uploads/2017/10/Banner-Kh%C3%B3a-h%E1%BB%8Dc-Ti%E1%BA%BFng-Anh-3.jpg" alt="">
                        </td>
                        <td class="item-title" >
                            <h3 style="color:#0071c5">Khóa học tiếng Nhật sơ cấp 1</h3>
                            <div style="float:left">
                                <p>Thời gian học dự kiến:</p>
                                <p>Giáo trình:</p>
                                <p>Giá khóa học:</p>
                            </div>
                            <div style="float:left;padding-left:40px;font-weight:600">
                                <p>12 tiếng</p>
                                <p>48 bài</p>
                                <p>200,000 Đồng</p>
                            </div>
                        </td>
                        <td class="item-close" style="width:10%" v-on:click="CloseItemCourse()">❌</td>
                    </tr>
                    <tr id="item-course">
                        <td class="item-image" >
                            <img class="" src="https://giuseart.com/wp-content/uploads/2017/10/Banner-Kh%C3%B3a-h%E1%BB%8Dc-Ti%E1%BA%BFng-Anh-3.jpg" alt="">
                        </td>
                        <td class="item-title" >
                            <h3 style="color:#0071c5">Khóa học tiếng Nhật sơ cấp 1</h3>
                            <div style="float:left">
                                <p>Thời gian học dự kiến:</p>
                                <p>Giáo trình:</p>
                                <p>Giá khóa học:</p>
                            </div>
                            <div style="float:left;padding-left:40px;font-weight:600">
                                <p>12 tiếng</p>
                                <p>48 bài</p>
                                <p>200,000 Đồng</p>
                            </div>
                        </td>
                        <td class="item-close" style="width:10%" v-on:click="CloseItemCourse()">❌</td>
                    </tr>
                    
                    <tr>
                        <td class="item-total"><p>Tổng tiền:<span><b> 2,500,000 </b></span></p></td>
                        <td></td>
                    </tr>
                    </table>
                    <button class="submit">Đăng ký khóa học</button>
                </div>
            </div>

        </div>
    </div>
</template>
<script>
export default {
  name: 'TeacherInfo',
  props: {
    msg: String
  },
  data(){
      return{
          content : true,
          catalog : true,
          DetailCourse : {},
          cartadd: { id: "", name: "", price: "", image: "", },
      }
  },
  methods: {
      Toggle(value){
          if(value == "content"){
              this.content = !this.content;
          }else{
              this.catalog = !this.catalog;
          }
      },
      OpenModal(){
          document.getElementById("myModal-Cart").style.display = "block"
      },
      CloseModal(){
          document.getElementById("myModal-Cart").style.display = "none"
      },
      CloseItemCourse(){
          document.getElementById("item-course").style.display = "none"
      },
      added(id,name,price,image){
             // cartadd is here to get all things that click or chosen by user 
             this.cartadd.id = id; 
             this.cartadd.name = name; 
             this.cartadd.price = price; 
             this.cartadd.image = image; 
             this.cartadd.qty = 1; 
             this.cart.push(this.cartadd); 
             this.cartadd = {}; 
             this.saveCats(); // this function most important to save all inform of products 
        },
        saveCats() {
        // for save in local storage set the below code 
            let parsed = JSON.stringify(this.cart); 
            localStorage.setItem("cart", parsed); 
            this.viewCart(); // by this function we can see all products are save in web },
        },
  },
  created() {
    this.DetailCourse = 
    {
"courseId": 5636,
"teacher" :
            {
                "userName"   : "Phan Minh Tài" ,
                "synopsis"	  : "giáo viên dạy tiếng Nhật giao tiếp 1",
                "coverImage" : "https://static2.yan.vn/YanNews/2167221/201704/20170428-104537-samsung-galaxy-j7-selfie_600x450.jpg",
                "gender"     : 0,
                "totalStudent" : 46,
            },
           

"courseName" : "Tiếng Nhật giao tiếp 1",
"courseSynopsis" : "Tiếng Nhật giao tiếp 1",
"totalStudent" : 31,
"courseEvaluate" : 4.5,
"courseCover" : "https://giuseart.com/wp-content/uploads/2017/10/Banner-Kh%C3%B3a-h%E1%BB%8Dc-Ti%E1%BA%BFng-Anh-3.jpg",
"coursePrice" : 9000000,
"offSelf" : 20,
"coursePriceDiscount" : 6000000,
"courseEstimatedStudyTime" : "2021-13-13",
"courseCurriculumTotal" : 10,
"coursePriceDiscountTime" : "2021-9-17",
"courseContentDetails" : "Tiếng Nhật giao tiếp 1",
"courseListCurrilum" : "Tiếng Nhật giao tiếp 1"
    }
 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
    width: 100%;
}
.flex-container {
  display: flex;
}

.flex-container > .media-teacher {
  background-color:#000044 ;
  padding: 20px;
  width:15%;
}
.flex-container > .media-teacher .box-media img{
    width: 100%;
    height: 100%;
}
.flex-container > .media-teacher .valuate-teacher p{
    font-size: 30px;
    font-weight: 700;
    color: #ffc700;
}
.flex-container  .media-teacher .detail_course{
    color:#ffff;
}
.flex-container  .media-teacher .box-text .name-teacher{
    font-size: 20px;
    color: #ffff;
    text-align: center;
}
.flex-container  .media-teacher .box-text  .icon-student{
    display: inline-block;
    vertical-align: middle;
}
.flex-container  .media-teacher .box-text  .number-student{
    display: inline-block;
    color: #ffff;
    vertical-align: middle;
    font-size: 20px;
    padding-left: 20px;
}
.flex-container > .detail_course {
  background-color: #000044;
  padding: 20px;
  width:80%;
}
.flex-container .detail_course h3 {
  color: #ffff;
  font-size: 20px;
  padding: 5px;
}
.flex-container .detail_course p {
  color: #ffff;
  font-size: 20px;
  padding: 5px;
}
.flex-container > .media-course {
  margin: 10px;
  padding: 20px;
  width:50%;
}
.flex-container .media-course .box-media-course img{
  border : 1px solid #000;
  width: 100%;
  height: 100%;
}
.flex-container .detail_info-course{
  margin: 10px;
  padding: 20px;
  width:50%;  
}
.flex-container .detail_info-course .price h3{
  font-size: 24px;
  font-weight: 600;
}
.flex-container .detail_info-course .price .cost{
  font-size: 30px;
  font-weight: 600;
  color: rgb(250, 18, 18);
}
.flex-container .detail_info-course .info p{
  font-size: 20px;
  font-weight: 500;
}
.detail_info-course .box-info span #cart{
    padding: 15px 25px;
    background-color: #000099;
    border-radius: 10px;
    text-decoration: none;
    color: #ffff;
    font-size: 20px;
    margin: 10px 10px 10px 0px;
    font-weight: 600;
}
.detail_info-course .box-info span #sub{
    padding: 15px 25px;
    background-color: #FF3300;
    border-radius: 10px;
    text-decoration: none;
    color: #ffff;
    font-size: 20px;
    margin: 10px 10px 10px 0px;
    font-weight: 600;
}
.content-course .content{
    padding: 10px 20px;
}
.header-tab h3{
    background-color:#DDDDDD;
    padding: 10px;
    font-weight: 400;
}
.header-tab span{
    float: right;
    cursor: pointer;
    line-height: 5px;
}
.header-tab p{
    margin: 0px;
}
.catalog-course .content{
    padding: 10px 20px;
}
.lesson_content{
    width: 100%;
}
.lesson_content tr td{
    padding: 10px 50px;
    font-size: 16px;
}
/* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  padding-top: 100px; /* Location of the box */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

/* Modal Content */
.modal-content {
  background-color: #fefefe;
  margin: auto;
  padding: 20px;
  border: 1px solid #888;
  width: 70%;
  border-radius: 10px;
}

/* The Close Button */
.close {
  color: #aaaaaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
}
.modal-content .item-image img{
    width: 150px;
}
.modal-content .item-close{
    font-size: 150%;
    cursor: pointer;
}
.modal-content .item-total p{
    font-size: 20px;
    padding: 10px 0px;
}
.modal-content .item-total span{
    color: #FF3300;
}
.modal-content .cart-content .submit{
    padding: 10px 20px;
    background: #0071c5;
    border: none;
    color: #ffff;
    font-size: 20px;
    border-radius: 5px;
    display: block;
    margin: 0px auto;
    cursor: pointer;
}
.shopping-cart .button-icon{
    position: fixed;
    right: 10px;
    bottom: 10px;
}
.shopping-cart .button-icon img{
    width: 60px;
    cursor: pointer;
}
.shopping-cart .button-icon .total-item-cart{
    background-color: #ffff;
    border: 1px solid #000;
    padding: 5px;
    border-radius: 20px;
    position: absolute;
    right: 0px;
}
/* Price */
   .style-1 del {
    color: blue;
    text-decoration: none;
    position: relative;
    font-size: 25px;
    font-weight: 700;
   }
    .style-1 del ::before {
      content: " ";
      display: block;
      width: 100%;
      border-top: 2px solid #cb0d0d;
      height: 12px;
      position: absolute;
      bottom: 0;
      left: 0;
      transform: rotate(-7deg);
    }
  ins {
    color: #cb0d0d;
    font-size: 35px;
    text-decoration: none;
    padding: 1em 1em 1em .5em;
    font-weight: 700;
  }
@media only screen and (max-width: 1100px) {
    .flex-container > .media-teacher{
        width: 30%;
    }
    /* Price */
   .style-1 del{
       font-size: 20px;
   }
   ins {
       font-size: 25px;
   }
}
@media only screen and (max-width: 600px) {
    .flex-container {
    display: flex;
    flex-direction: column;
    }
    .flex-container > .media-teacher {
    background-color:#000044 ;
    padding: 20px;
    width:100%;
    }
    .flex-container > .detail_course {
    background-color: #000044;
    padding: 20px;
    width:100%;
    }
    .flex-container > .media-course {
    margin: 0px;
    padding: 0px;
    width:100%;
    }
    .flex-container .detail_info-course{
    margin: 0px;
    padding: 10px;
    width:100%;  
    }
    .detail_info-course .box-info span #cart{
        width: 80%;
    }
    .detail_info-course .box-info span #sub{
        width: 80%;
    }
    /* Modal Content */
    .modal-content {
    background-color: #fefefe;
    margin: auto;
    padding: 20px;
    border: 1px solid #888;
    width: 90%;
    }
    .modal-content .cart-content .cart-table td{
        display: block;
    }
    .lesson_content tr td{
        padding: 10px;
    }
    /* Price */
   .style-1 del{
       font-size: 20px;
   }
   ins {
       font-size: 25px;
   }
}
</style>
