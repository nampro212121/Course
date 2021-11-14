<template>
    <div class="container-home">
        <div id="sideNavigation" class="sidenav">
        <a href="javascript:void(0)" class="closebtn"  v-on:click="closeNav()">&times;</a>
            <div  class="" v-for="catalog in catalogs[0].listCatalog" :key="catalog.id">
                 <a>{{ catalog.name }}</a>
            </div>
        </div>
        <nav class="topnav">
            <div class="subscribe">
                <a>Đăng ký học</a>
            </div>
            <div class="nav-list">
                <div>
                 <carousel class="catalog-desk"  :items-to-show="5">
                    <slide v-for="catalog in catalogs[0].listCatalog" :key="catalog.id">
                    <a href="">{{ catalog.name }}</a>
                    </slide>
                    <template #addons>
                    <navigation />
                    </template>
                </carousel>
                </div>
                <div class="catalog-mobile">
                    <a  href="#" v-on:click="openNav()">
                    Danh mục
                    </a>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation } from 'vue3-carousel';

// import axios from 'axios'
export default {
  name: 'Home',
  components:{
    Carousel,
    Slide,
    Navigation,
  },
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
 }
}

</script>
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
  padding: 0px !important;
  margin: 0px !important;
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
    padding: 12px 14px;
    margin: 5px;
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
    transform: rotate(-5deg);
    color: #00CC66;
    border-radius: 10px;
    margin-left: 10px;
    cursor: pointer;
    font-weight: 600;
    font-size: 24px;
}
.topnav .catalog-mobile{
    display: none;
    
}
.catalog-mobile a{
     background-image: linear-gradient(135deg,#02adff,#00d3ff);
    border-radius: 10px;
    margin-right: 10px;
    float: right;
    cursor: pointer;
    font-weight: 600;
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
.carousel__slide{
    width: auto !important;
}
.carousel__prev{
    display: none !important;
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

</style>