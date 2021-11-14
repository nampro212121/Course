<template>
  <div class="container-home">
     <div id="sideNavigation" class="sidenav">
        <a href="javascript:void(0)" class="closebtn"  v-on:click="closeNav()">&times;</a>
            <div  class="" v-for="catalog in catalogs[0].listCatalog" :key="catalog.id">
                 <a>{{ catalog.name }}</a>
            </div>
     </div>
     <main id="container" >
    <div class="header">
        <div class="header-maxwidth">
            <div class="logo">
                <img src="../assets/logo-jp.png" alt="">
            </div>
        </div>
    </div>
      <nav class="topnav">
        <div class="nav-list">
            <div class="subscribe">
                <a>Đăng ký học</a>
            </div>
            <div class="catalog-desk" v-for="catalog in catalogs[0].listCatalog" :key="catalog.id">
                <a href="">{{ catalog.name }}</a>
            </div>
            <div class="catalog-mobile">
                <a  href="#" v-on:click="openNav()">
                Toàn bộ
                </a>
            </div>
        </div>
      </nav>
      <div id="">
    
      </div>
      <!-- Banner -->
      <div class="image-banner">
        <img src="../assets/VN5.jpg">
      </div>
      <!-- List Course -->
      <div class="container">
        <!-- Hot Course -->
        <div class="list-course">
          <img src="../assets/icon-st.afa7ee3.jpg" class="image-title" alt="">
          <div class="title-tyte-course">Danh sách khóa học được nhiều học viên lựa chọn</div>
          <div class="row">
              <div v-for="hotCourse in catalogs[0].listHotCouse" :key="hotCourse.id">
                    <div class="column">
                        <div class="card">
                            <div class="image-course">
                                <img :src="''+hotCourse.courseCover" alt="">
                            </div>
                            <div class="info-course">
                                <div class="star-rating"></div>
                                <div class="price-course">{{hotCourse.coursePriceDiscount}}<span> VNĐ</span></div>
                            </div>
                            <div class="title-course">
                                {{hotCourse.courseName}}
                            </div>
                        </div>
                    </div>
              </div>
              <div class="pagination">
                    <a href="#">&laquo;</a>
                    <a href="#">1</a>
                    <a href="#" class="active">2</a>
                    <a href="#">3</a>
                    <a href="#">4</a>
                    <a href="#">5</a>
                    <a href="#">6</a>
                    <a href="#">&raquo;</a>
               </div>
        </div>
        </div>
        <!-- New Course -->
        <div class="list-course">
          <img src="../assets/icon-st.afa7ee3.jpg" class="image-title" alt="">
          <div class="title-tyte-course">Danh sách khóa học mới nhất có thể đăng ký học</div>
          <div class="row">
            <div v-for="newCourse in catalogs[0].listNewCouse" :key="newCourse.id">
                    <div class="column">
                        <div class="card">
                            <div class="image-course">
                                <img :src="''+newCourse.courseCover" alt="">
                            </div>
                            <div class="info-course">
                                <div class="star-rating"></div>
                                <div class="price-course">{{newCourse.coursePriceDiscount}}<span> VNĐ</span></div>
                            </div>
                            <div class="title-course">
                                {{newCourse.courseName}}
                            </div>
                        </div>
                    </div>
            </div>
        </div>
        </div>
        <!-- Encourage Course -->
        <div class="list-course">
          <img src="../assets/icon-st.afa7ee3.jpg" class="image-title" alt="">
          <div class="title-tyte-course">Danh sách khóa học được khuyến khích bởi Stuydy-Arts</div>
          <div class="row">
            <div v-for="encourageCourse in catalogs[0].listEncourage" :key="encourageCourse.id">
                    <div class="column">
                        <div class="card">
                            <div class="image-course">
                                <img :src="''+encourageCourse.courseCover" alt="">
                            </div>
                            <div class="info-course">
                                <div class="star-rating"></div>
                                <div class="price-course">{{encourageCourse.coursePriceDiscount}}<span> VNĐ</span></div>
                            </div>
                            <div class="title-course">
                                {{encourageCourse.courseName}}
                            </div>
                        </div>
                    </div>
            </div>
        </div>
        </div>
      </div>
     </main>
  </div>
</template>

<script>
// import axios from 'axios'
export default {
  name: 'Home',
  props: {
    msg: String
  },
  setup(){
    const openNav = ()=> {
    document.getElementById("sideNavigation").style.width = "350px";
    document.getElementById("main").style.marginLeft = "250px";
    }
    const closeNav = ()=> {
    document.getElementById("sideNavigation").style.width = "0";
    document.getElementById("main").style.marginLeft = "0";
    }
        return{
            openNav,closeNav,
            catalogs: [],
        }
    },
 
  created() {
      
    this.catalogs = [{
    "listCatalog":[
              {
                  "id": 1,
                  "name": "Tiếng Nhật",
                  "order": 1,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 2,
                  "name": "Tiếng Anh",
                  "order": 2,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 3,
                  "name": "Lập trình",
                  "order": 3,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 4,
                  "name": "Kinh tế",
                  "order": 4,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 5,
                  "name": "Quản trị kinh doanh",
                  "order": 5,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 6,
                  "name": "Tin học ứng dụng",
                  "order": 6,
                  "created_at": null,
                  "updated_at": null
              },
              {
                  "id": 7,
                  "name": "Xã hội",
                  "order": 7,
                  "created_at": null,
                  "updated_at": null
              }],
 "listNewCouse":[
              {
                  "courseId": 468230,
                  "catalogId": 12345,
                  "courseCover" : "https://zshop.vn/blogs/wp-content/uploads/2018/01/720x360.jpg",
                  "courseEvaluate ": 2,
                  "coursePrice" : 350000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 150000,
                  "courseName": "Phát triển khả năng lập trình",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468231,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSFATteACV8noSGOy0RHHMUm-icyYVZ4z8bQ6ngKyk943HhnePamRA_E1pMRN0y3x33104&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 1025000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 1560000,
                  "courseName": "Hán tự cơ bản",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468232,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSp30oitiXJVwIitlepLqa_fFGc0n-X17XaHf4t4UfzMyY8bfU_P3Y5j1xA9uN-7_MptKE&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 1452000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 520000,
                  "courseName": "Tiếng Anh cơ bản cho người mới bắt đầu",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468233,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSeDjFlBlS_CZClMtJWwNqJHbe6O3SYZUuiuxCQItRYu9XGFJjUEA6_zULmzaNdFb72tEE&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 2500000,
                  "courseName": "Dạy học làm giàu",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },],
  "listHotCouse":[
              {
                  "courseId": 697340,
                  "catalogId": 12345,
                  "courseCover" : "https://office-softech.cdn.vccloud.vn/ckfinder/userfiles//files/C_Users_Chi_AppData_Local_Packages_Microsoft_SkypeApp_kzf8qxf38zg5c_LocalState_284a7d12-dbb1-45aa-9d1d-f66f3484ed43.png",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 399900,
                  "courseName": "Lập trình web từ cơ bản đến nâng cao",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 697341,
                  "catalogId": 12345,
                  "courseCover" : "https://cdn-www.vinid.net/dc2a973f-hocmai_web.jpg",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 456000,
                  "courseName": "Xây dựng và hợp tác kinh doanh",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 697342,
                  "catalogId": 12345,
                  "courseCover" : "https://salt.tikicdn.com/ts/tmp/25/82/a9/af2f4dc6b1314238397e3fbd0040d0b1.jpeg",
                  "courseEvaluate ": 2,
                  "coursePrice" : 245000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 354000,
                  "courseName": "Tiếng Nhật giao tiếp 1",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 697343,
                  "catalogId": 12345,
                  "courseCover" : "http://hoctot.hocmai.vn/wp-content/uploads/2019/06/live-1.png",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 556000,
                  "courseName": "Khóa học Facebook Marketing từ A - Z",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468230,
                  "catalogId": 12345,
                  "courseCover" : "https://hoctot.hocmai.vn/wp-content/uploads/2021/09/715x400-master.png",
                  "courseEvaluate ": 2,
                  "coursePrice" : 350000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 150000,
                  "courseName": "Phát triển khả năng lập trình",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468231,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSN-epMwkxDJERXx_Ax5kzZfQgySIfistPLITezkXSX7YRDO4epMNzd6SNw7sGAK-WgkaU&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 1025000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 1560000,
                  "courseName": "Hán tự cơ bản",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468232,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSIgtEQrGJJJRhD3bsBbcjfDFLKUmP1wOCk69aW-FQqEPxhzsTS7auHWOr-NF6P6nZ71Rc&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 1452000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 520000,
                  "courseName": "Tiếng Anh cơ bản cho người mới bắt đầu",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 468233,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-q-svgyMCggloriyDyH1nDAKc1Yx9m3IsqJIjUw5eU51mIrLy0pmurGBRnya_YIK8UOc&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 2500000,
                  "courseName": "Dạy học làm giàu",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              ],
    "listEncourage":[
               {
                  "courseId": 74560,
                  "catalogId": 12345,
                  "courseCover" : "https://hoctot.hocmai.vn/wp-content/uploads/2021/09/715x400-master.png",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 550000,
                  "courseName": "Khóa học 15 ngày trở thành đỉnh cao trong phân tích kỹ thuật chứng khoán",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 74561,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTwLBS52MsPb9mnaTMZzM30geZqi-zF9MEJCA&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 240000,
                  "courseName": "Khoá học 7 ngày giảm cân an toàn",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 74562,
                  "catalogId": 12345,
                  "courseCover" : "https://hoctot.hocmai.vn/wp-content/uploads/2021/09/715x400-master.png",
                  "courseEvaluate ": 2,
                  "coursePrice" : 1010000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 1010000,
                  "courseName": "Khoá học 65 Tuyệt chiêu quảng cáo Google Ads đỉnh cao giúp bạn tiết kiệm 50% ngân sách",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },
              {
                  "courseId": 74563,
                  "catalogId": 12345,
                  "courseCover" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQdRj0yRiTlwkGFLPKeYH4mLNn3HEBG6IR2F-LBeGHpDnxGg7EtqXLLnmWHBV7NG3A1lP4&usqp=CAU",
                  "courseEvaluate ": 2,
                  "coursePrice" : 200000,
                  "offSelf" : 20,
                  "coursePriceDiscount": 150000,
                  "courseName": "Dạy học làm giàu",
                  "totalStudent" : 4,
                  "courseUpdateDate" : '20210709 12:00:00',     
              },]

  }]
  console.log(this.catalogs[0].listNewCouse)
 }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* The side navigation menu */
  h3{
    cursor: pointer;
  }
  #text{
    position: absolute;
    top: 50%;
    left: 50%;
    font-size: 50px;
    color: white;
    transform: translate(-50%,-50%);
    -ms-transform: translate(-50%,-50%);
  }
.sidenav {
    height: 100%; /* 100% Full-height */
    width: 0; /* 0 width - change this with JavaScript */
    position: fixed; /* Stay in place */
    z-index: 1; /* Stay on top */
    top: 0;
    left: 0;
    background-color: #ffffff; /* Black*/
    overflow-x: hidden; /* Disable horizontal scroll */
    padding-top: 60px; /* Place content 60px from the top */
    transition: 0.5s; /* 0.5 second transition effect to slide in the sidenav */
}

/* The navigation menu links */
.sidenav p {
    padding: 8px 8px 0px 32px;
    text-decoration: none;
    font-size: 20px;
    color: #000;
    display: block;
    transition: 0.3s;
    font-weight: 600;
}
.sidenav a {
    padding: 8px 8px 8px 32px;
    text-decoration: none;
    font-size: 20px;
    color: #000;
    display: block;
    transition: 0.3s;
    font-weight: 400;
    cursor: pointer;
}

/* When you mouse over the navigation links, change their color */
.sidenav a:hover, .offcanvas a:focus{
    color: #7e6a6a;
}

/* Position and style the close button (top right corner) */
.sidenav .closebtn {
    position: absolute;
    top: 0;
    right: 25px;
    font-size: 36px;
    margin-left: 50px;
}

/* Style page content - use this if you want to push the page content to the right when you open the side navigation */
#main {
    transition: margin-left .5s;
    padding: 20px;
    overflow:hidden;
    width:100%;
}
body {
  overflow-x: hidden;
  font-family : arial !important;
  padding: 0px;
  margin: 0px;
}
.header{
    width: 100%;
    z-index: 99;
    transition: .5s ease;
    top: 0;
    background-color: #0071c5;
    height: 60px;
}
.header-maxwidth{
    display: flex;
    position: relative;
    -ms-flex-align: center;
    align-items: center;
    -ms-flex-pack: justify;
    justify-content: space-between;
    height: 60px;
    width: calc(100% - 40px);
    margin: 0 auto;
    max-width: 1200px;
}
/* Add a black background color to the top navigation */
.topnav {
    background-color: #050d79;
    overflow: hidden;
}
.topnav .nav-list{
    margin: 0px auto;
    display: block;
}
/* Style the links inside the navigation bar */
.topnav a {
    float: left;
    display: block;
    color: rgb(255, 255, 255);
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 22px;
}
/* Change the color of links on hover */
.topnav a:hover {
    background-color: #ddd;
    color: black;
    border-radius: 10px;
}

/* Add a color to the active/current link */
.topnav a.active {
    background-color: #4CAF50;
    color: white;
}
.subscribe a{
    background: rosybrown;
    border-radius: 10px;
    margin: 0px 20px;
    cursor: pointer;
    font-weight: 600;
}
.topnav .catalog-mobile{
    display: none;
}
@media screen and (max-width: 600px) {
   .topnav .catalog-mobile{
        display: block;
    }
    .topnav .catalog-desk{
        display: none;
    }
}
@media screen and (max-height: 450px) {
    .sidenav {padding-top: 15px;}
    .sidenav a {font-size: 18px;}
   
    
}
.course{
    color: #808080;
}
/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */


a svg{
  transition:all .5s ease;

  &:hover{
    #transform:rotate(180deg);
  }
}

#ico{
  display: none;
}

.menu{
  background: #000;
  display: none;
  padding: 5px;
  width: 320px;
  @include border-radius(5px);

  #transition: all 0.5s ease;

  a{
    display: block;
    color: #fff;
    text-align: center;
    padding: 10px 2px;
    margin: 3px 0;
    text-decoration: none;
    background: #444;

    &:nth-child(1){
      margin-top: 0;
      @include border-radius(3px 3px 0 0 );
    }
    &:nth-child(5){
      margin-bottom: 0;
      @include border-radius(0 0 3px 3px);
    }

    &:hover{
      background: #555;
    }
  }
}

.image-banner{
    width:100px;
}
.image-banner img{
    max-width: 1349px;
    height: auto;
}
.container{
    margin: 0 auto;
    width: 100%;
    max-width: 100%;
    padding: 0;
    box-sizing: border-box;
    max-width: 1200px;
}
.list-course{
    width: 100%!important;
    background: #fff;
    border-radius: 6px;
    border: 1pxsolid #e3e3e3;
    padding: 10px;
    margin: 40px 0px;
    box-shadow: 0 12px 18px #dadae8;
}
.title-tyte-course{
    display: inline-block;
    font-size: 24px;
    padding: 10px 20px 10px 10px;
    line-height: 35px;
    cursor: pointer;
    font-weight: 700;
}
.list-course .image-title{
    display: inline-block;
    height: 30px !important;
    width: 30px !important;
    margin-top: 0 !important;
}
.list-course .image-course{
    height: 116px !important;
    width: 100%!important;
    overflow: hidden!important;
    border-radius: 4px 4px 0 0;
    margin-bottom: 10px;
}
.list-course .image-course img{
    height: 100%;
    object-fit: contain;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
.list-course .title-course{
    -webkit-line-clamp: 2!important;
    padding: 0 10px!important;
    cursor: pointer!important;
    color: #0071c5!important;
    margin: 10px 0 0!important;
    font-size: 16px!important;
    font-weight: 700!important;
    display: -webkit-box;
    overflow: hidden;
}
.list-course .star-rating{
    font-size: 0;
    position: relative;
    display: inline-block;
}
.list-course .info-course{
    border-bottom: 1px solid #0071c5;
}
 .list-course .star-rating::before {
    content: "\f005\f005\f005\f005\f005";
    font-family: FontAwesome;
    font-size: 15px;
    color: #cb0d0d;
 }
 .list-course .price-course{
     display: inline-block;
     font-weight: 700;
     float: right;
 }
 .pagination {
  display: inline-block;
  margin: 20px auto;
}

.pagination a {
  color: black;
  float: left;
  padding: 8px 16px;
  text-decoration: none;
  transition: background-color .3s;
  border: 1px solid #ddd;
  margin: 0 4px;
  border-radius: 10px;
}

.pagination a.active {
  background-color: #0071c5;
  color: white;
  border: 1px solid #0071c5;
}

.pagination a:hover:not(.active) {background-color: #ddd;}  
/* Float four columns side by side */
.column {
  float: left;
  width: 23%;
  padding: 10px 10px;
}

/* Remove extra left and right margins, due to padding in columns */
.row {margin: 0 -5px;}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Style the counter cards */
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* this adds the "card" effect */
  padding: 16px;
  text-align: left;
  background-color: #f1f1f1;
  height: 230px;
}

/* Responsive columns - one column layout (vertical) on small screens */
@media screen and (max-width: 900px) {
  .column {
    width: 45%;
    display: block;
    margin-bottom: 20px;
  }
}

</style>
