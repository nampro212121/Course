<template>
  <div class="container-comment">
    <div class="header-tab">
        <h3>Nhận xét của học viên<!--  -->
            <span><p v-on:click="Toggle('comment')">&#128317;</p></span>
        </h3>
    </div>
    <div class="add-comment">
        <button v-on:click="OpenModal()">Thêm đánh giá của bạn về khóa học</button>
        <!-- The Modal -->
        <div id="myModal" class="modal">

            <!-- Modal content -->
            <div class="modal-content">
                <span v-on:click="CloseModal()" class="close">&times;</span>
                <p class="title-course">Khóa sơ cấp (khóa học N5, N4)</p>
                <form class="comment-form" action="" method="post">
                    <div class="rating">
                        <div class="rate">
                            <p class="title-comment">Đánh giá của bạn về khóa học</p>
                            <input type="radio" id="star5" name="rate" value="5" />
                            <label for="star5" title="text"></label>
                            <input type="radio" id="star4" name="rate" value="4" />
                            <label for="star4" title="text"></label>
                            <input type="radio" id="star3" name="rate" value="3" />
                            <label for="star3" title="text"></label>
                            <input type="radio" id="star2" name="rate" value="2" />
                            <label for="star2" title="text"></label>
                            <input type="radio" id="star1" name="rate" value="1" />
                            <label for="star1" title="text"></label>
                        </div>
                    </div>
                    <div class="comment-fill">
                        <p class="title-comment">Cảm nhận của bạn về khóa học này</p>
                        <textarea name="" id="" cols="30" rows="10"></textarea>
                    </div>
                    <button class="submit">Gửi đánh giá</button>
                </form>
            </div>

        </div>
    </div>
    <div class="comment"  v-for="comments in ApiComment[0].userInfo" :key="comments.userId">
        <div class="comment-item">
            <img class="avatar-student" :src="comments.headImagePath">
            <div class="info-comment">
                <p class="item-name">{{comments.name}}</p>
                <a class="item-rating">&#9733;&#9733;&#9733;&#9733;&#9734;</a>
                <p class="item-time">{{comments.timeComment}}</p>
            </div>
        </div>
        <div class="comment-content">
            <p>{{comments.comment}}</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
      return{
          comment : true,
          ApiComment: [],
      }
  },
   created() {
    this.ApiComment = [
        {
        "userInfo" :[
            {
                "userId"   : 76590 ,
                "name"	  : "Lê Thị Thanh Thảo",
                "headImagePath" : "https://upanh123.com/wp-content/uploads/2021/02/hinh-anh-hoc-sinh-cap-39.png",
                "gender"     : 1,
                "evaluate" : 1,
                "comment"	: "Bức ảnh thật đẹp. Tôi xin chân thành cảm ơn tới các ban ngành, lãnh đạo,cảm ơn ông Nguyễn Tấn Dũng và đoàn thể nhà nước Việt Nam đã cho tôi được thấy hình ảnh này,xin cảm ơn Mark Zuckerberg, người đồng sáng lập ra facebook, cảm ơn nước Mỹ vì đã sinh ra 1 con người thông minh và xuất sắc như thế này, để tôi xem được bức ảnh đẹp thế này cũng phải cảm ơn đến Bill Gates, người đồng sáng lập ra microsoft windows xp, cảm ơn cha và mẹ ông cũng như người vợ yêu quý của ông, cảm ơn tổng thống nước mỹ, cảm ơn nhà nước liên xô cũ đã giúp Việt Nam chúng tôi xây dựng thành công đập thủy điện Hòa Bình và mang điện đến cho chúng tôi thắp sáng, nấu cơm cũng như là có điện để chạy máy tính lên facebook xem ảnh này, xin chân thành cảm ơn đến bố, mẹ đã sinh ra tôi, cảm ơn các thầy cô đã dạy cho tôi biết chữ, biết viết văn, làm toán, dạy tôi làm người tốt.",
                "timeComment" : "2021-08-12"
                },
            {
                "userId"   : 76591 ,
                "name"	  : "Lê Đức Huy",
                "headImagePath" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRF03K8Vbj-c07TwXxnOQEd9iDecg1IruQW4A&usqp=CAU",
                "gender"     : 0,
                "evaluate" : 5,
                "comment"	: "Bức ảnh thật đẹp. Tôi xin chân thành cảm ơn tới các ban ngành, lãnh đạo,cảm ơn ông Nguyễn Tấn Dũng và đoàn thể nhà nước Việt Nam đã cho tôi được thấy hình ảnh này,xin cảm ơn Mark Zuckerberg, người đồng sáng lập ra facebook, cảm ơn nước Mỹ vì đã sinh ra 1 con người thông minh và xuất sắc như thế này, để tôi xem được bức ảnh đẹp thế này cũng phải cảm ơn đến Bill Gates, người đồng sáng lập ra microsoft windows xp, cảm ơn cha và mẹ ông cũng như người vợ yêu quý của ông, cảm ơn tổng thống nước mỹ, cảm ơn nhà nước liên xô cũ đã giúp Việt Nam chúng tôi xây dựng thành công đập thủy điện Hòa Bình và mang điện đến cho chúng tôi thắp sáng, nấu cơm cũng như là có điện để chạy máy tính lên facebook xem ảnh này, xin chân thành cảm ơn đến bố, mẹ đã sinh ra tôi, cảm ơn các thầy cô đã dạy cho tôi biết chữ, biết viết văn, làm toán, dạy tôi làm người tốt.",
                "timeComment" : "2021-09-23"
                },
            {
                "userId"   : 76592 ,
                "name"	  : "Trần Thanh Bình",
                "headImagePath" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcThGynWdjo9Pvsw2A9xcO3Cus16ojfeoOejVQ&usqp=CAU",
                "gender"     : 0,
                "evaluate" : 4,
                "comment"	: "Khóa học này rất đáng để học",
                "timeComment" : "2021-09-23"
                },
            {
                "userId"   : 76593 ,
                "name"	  : "Nguyễn Ngọc Nhân",
                "headImagePath" : "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRfpua_IlDLbLk_U_7i4aUAUlZCubT64rh9ZA&usqp=CAU",
                "gender"     : 0,
                "evaluate" : 2,
                "comment"	: "Khóa học này rất đáng để học",
                "timeComment" : "2021-09-23"
                }
                ],
        "totalComment"	: 4
        }
    ]
    },
  methods: {
      Toggle(value){
          if(value == "comment"){
              this.comment = !this.comment;
            }
      },
      OpenModal(){
          document.getElementById("myModal").style.display = "block"
      },
      CloseModal(){
          document.getElementById("myModal").style.display = "none"
      }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
.container-comment .comment{
    display: flex;
    border: 1px solid #0071c5;
    margin: 10px;
    border-radius: 20px;
}
.container-comment > .comment .comment-item {
    padding: 5px;
    width: 30%;
    display:flex;
    align-items: center;
}
.container-comment > .comment .comment-item .avatar-student{
    padding: 5px;
    width: 70px;
    height:70px;
    border-radius: 50%;
    margin-right: 20px;
}
.container-comment > .comment .comment-content {
  cursor: pointer;
  padding: 10px;
  width: 80%;
    display: -webkit-box;
    max-height: 6.2rem;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: normal;
    -webkit-line-clamp: 4;
    line-height: 1.6rem;
    transition-delay: 2s;
}
.container-comment > .comment .comment-content:hover{
  display: block;
  max-height: none;
}
.info-comment{
    padding: 5px;
}
.item-rating{
    font-size: 150%;
    color: #cb0d0d;
}
.item-time{
    color:  #999;
}
.container-comment .add-comment  button{
    padding: 10px 20px;
    background: #000099;
    border: none;
    color: #ffff;
    font-size: 24px;
    border-radius: 5px;
    display: block;
    margin: 0px auto;
    cursor: pointer;
    
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
  width: 50%;
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
.rate {

}
.rate:not(:checked) > input {
 float:left;
 display: none;
}
.rate:not(:checked) > label {
    display: right;
    width:1em;
    overflow:hidden;
    white-space:nowrap;
    cursor:pointer;
    font-size:30px;
    color:#ccc;
}
.rate:not(:checked) > label:before {
    content: '★ ';
    font-size: 100%
}
.rate > input:checked ~ label {
    color: #ffc700;    
}
.rate:not(:checked) > label:hover,
.rate:not(:checked) > label:hover ~ label {
    color: #deb217;  
}
.rate > input:checked + label:hover,
.rate > input:checked + label:hover ~ label,
.rate > input:checked ~ label:hover,
.rate > input:checked ~ label:hover ~ label,
.rate > label:hover ~ input:checked ~ label {
    color: #c59b08;
}
#myModal .modal-content .title-course{
    font-size: 22px;
    font-weight:600;
    color: #007aff;
}
#myModal .modal-content .title-comment{
    font-family: Arial, Helvetica, sans-serif;
    color: #666666;
}
.comment-form .comment-fill textarea{
        width: 100%;
        border: 1px solid #007aff;
}
@media only screen and (max-width: 600px) {
    .container-comment .comment{
        display: flex;
        flex-direction: column;
    }
    .container-comment > .comment .comment-item {
        display: flex;
        width: 100%;
    }
    .container-comment > .comment .comment-content {
        width: 100%;
    }
    .modal-content {
        background-color: #fefefe;
        margin: auto;
        padding: 20px;
        border: 1px solid #888;
        width: 90%;
    }
}
</style>
