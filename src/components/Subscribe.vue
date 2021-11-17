<template>
  <div class="container-subscribe">
       <div class="step-progress">
           <div class="progress-container">
            <div class="progress"></div>
            <div class="circle active">Đăng ký</div>
            <div class="circle">Chuyển khoản</div>
            <div class="circle">Vào học</div>
       </div>
       </div>
       <div class="info-pay">
        <div class="header-tab">
            <h3>Thông tin chuyển khoản<!--  -->
            </h3>
            <div class="main">
                <div class="info-transfer" >
                    <div class="info-bank">
                        <div class="info">
                        <p class="ty">Công ty ACB</p>
                        <p class="ty">Số tài khoản <span><b>12344354678</b></span></p>
                        <p class="ty">Tên ngân hàng <span><b>Đông á Bank </b></span></p>
                        </div>
                        <div class="info">
                            <p class="ty">Công ty ACB</p>
                            <p class="ty">Số tài khoản <span><b>12344354678</b></span></p>
                            <p class="ty">Tên ngân hàng <span><b>Đông á Bank</b></span></p>
                        </div>
                        <div class="info">
                            <p class="ty">Công ty ACB</p>
                            <p class="ty">Số tài khoản <span><b>12344354678</b></span></p>
                            <p class="ty">Tên ngân hàng <span><b>Đông á Bank</b></span></p>
                        </div>
                        <div class="info">
                            <p class="ty">Công ty ACB</p>
                            <p class="ty">Số tài khoản <span><b>12344354678</b></span></p>
                            <p class="ty">Tên ngân hàng <span><b>Đông á Bank</b></span></p>
                        </div>
                    </div>
                    <div class="synthetic">
                        <p class="ty">Số tiền <span><b>600,000 Đồng</b></span></p>
                        <p class="ty">Nội dung chuyển khoản</p>
                    </div>
                </div>
                <div>
                    
                </div>
                <div class="form-sub">
                    <form action="action_page.php">
                        <div class="row">
                        <div class="col-25">
                            <label for="fname">Họ và tên<span>*</span></label>
                        </div>
                        <div class="col-75">
                            <input type="text" id="fname" name="firstname" >
                        </div>
                        </div>
                        <div class="row">
                        <div class="col-25">
                            <label for="lname">Địa chỉ mail<span>*</span></label>
                        </div>
                        <div class="col-75">
                            <input type="text" id="lname" name="lastname" >
                        </div>
                        </div>
                        <div class="row">
                        <div class="col-25">
                            <label for="lname">Số điện thoại<span>*</span></label>
                        </div>
                        <div class="col-75">
                            <input type="text" id="lname" name="lastname" >
                        </div>
                        </div>
                        <div class="row">
                            <p class="attention">Chú ý: bạn cần ghi chú lại nội dung chuyển khoản để dùng khi liên hệ với nhân viên Study-arts về nội dung đăng kí học</p>
                        </div>
                        <div class="row">
                        <input type="submit" value="Đăng ký khóa học">
                        </div>
                    </form>
                </div>
            </div>
        </div>
       </div>
       <div>
           <div class="header-tab">
                <h3>Thông tin khóa học đã đăng ký<!--  -->
                </h3>
                <!-- Add component -->
            </div>
       </div>
       <div class="detail-pay">
           <table>
               <tr>
                   <th>No.</th>
                   <th>Tên khóa học</th>
                   <th>Giá gốc</th>
                   <th>Số tiền đã giảm</th>
                   <th>Số tiền phải trả</th>
               </tr>
               <tr>
                   <td>1</td>
                   <td>Tiếng Nhật giao tiếp 1</td>
                   <td>500,000</td>
                   <td>400,000</td>
                   <td>400,000</td>
               </tr>
               <tr>
                   <td>12</td>
                   <td>Tiếng Nhật giao tiếp 2</td>
                   <td>500,000</td>
                   <td>400,000</td>
                   <td>400,000</td>
               </tr>
               <tr>
                   <td colspan="5" class="total">
                       <a href="" class="button-back">Quay lại</a>
                       <p>Tổng tiền: <span>800,000 Đồng</span></p>
                   </td>
               </tr>
           </table>
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
* {
  box-sizing: border-box;
}

.step-progress{
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
}
.progress-container{
  display: flex;
  justify-content: space-between;
  position: relative;
   max-width: 100%; 
  width: 550px;
  margin-bottom: 2.5em;
}
.progress-container::before{
content: "";
position: absolute;
top: 50%;
left: 0;
height: 4px;
width: 100%;
background-color: #BBBBBB;
z-index: -1;
}
.progress{
  position: absolute;
  top: 50%;
  left: 0;
  width: 0;
  height: 4px;
  background-color: var(--line-border-fill);
  z-index: -1;
  transition: all .5s ease-in;
}
.circle{
  background-color: #fff;
  height: 100px;
  width: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  transition: all .4s ease-in;
  border : 7px solid #AAAAAA;
}
.circle.active{
  border-color: #0071c5;
  background-color: #fff;
  box-shadow: 0px 0px 31px -2px rgba(0,105,37,0.62);
}
.header-tab h3{
    background-color:#DDDDDD;
    padding: 10px;
    font-weight: 400;
}
.info-pay .main{
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-content: center;
}
.info-pay .main .info-transfer{
    padding: 20px;
    font-size: 30px;
    width: 40%;
    border: 1px solid #0071c5;
}
.info-pay .main .info-transfer .info-bank{
    display:flex;
    flex-wrap: wrap;
}
.info-pay .main .info-transfer .info-bank .info{
    flex:45%;
    margin: 10px;
    box-shadow: 0px 20px 30px -20px hsl(229, 6%, 66%);
    border-radius: 5px;
    padding: 5px;
    border-top: 3px solid #0071c5;
}
.info-pay .main .info-transfer .title{
    text-align: center;
    color: #0071c5;
    font-weight: 400;
    font-size: 20px;
}
.info-pay .main .info-transfer .synthetic{
    border-top: 1px solid #0071c5;
    margin: 10px;
}
.info-pay .main .info-transfer .ty{
    color: #606266;
}
.info-pay .main .form-sub{
    padding: 20px;
    font-size: 30px;
    width: 55%;
}
/* Style inputs, select elements and textareas */
input[type=text]{
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  resize: vertical;
}

/* Style the label to display next to the inputs */
label {
  padding: 12px 12px 12px 0;
  display: inline-block;
}
label span{
    color:rgb(241, 12, 12);
}
/* Style the submit button */
input[type=submit] {
  background-color: #04AA6D;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  display: block;
  margin: 0px auto;
  font-size: 20px;
}
.form-sub form .attention{
    color: #606266;
    font-size: 16px;
    text-align: center;
    padding: 20px 0px;
}
/* Style the container */
.container {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}

/* Floating column for labels: 25% width */
.col-25 {
  float: left;
  width: 25%;
  margin-top: 6px;
}

/* Floating column for inputs: 75% width */
.col-75 {
  float: left;
  width: 75%;
  margin-top: 6px;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
.detail-pay{
    overflow-x: auto;
}
.detail-pay table{
    width: 1200px;
    margin: 20px auto;
    border-radius: 5px;
    box-shadow: 0px 30px 40px -20px hsl(229, 6%, 66%);
}
.detail-pay th {
    text-align: left;
    padding: 10px;
    color: #fff;
    background-color: #0071c5;
}
.detail-pay td {
    text-align: left;
    padding: 20px;
}
.detail-pay tr:nth-child(even){background-color: #f2f2f2;}
.detail-pay tr:hover {background-color: #ddd;}
.detail-pay table .total p{
    font-size: 18px;
    font-weight: 600;
    float: right;
}
.detail-pay table .total span{
    color: #cb0d0d;
}
.detail-pay table .total .button-back{
    text-decoration: none;
    background-color: #0071c5;
    color: #fff;
    font-size: 18px;
    padding: 10px 20px;
    border-radius: 5px;
}
/* Responsive layout - when the screen is less than 600px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .col-25, .col-75, input[type=submit] {
    width: 100%;
    margin-top: 0;
  }
  .info-pay .main .info-transfer{
    padding: 20px;
    font-size: 30px;
    width: 100%;
    border: 1px solid #0071c5;
   }
   .info-pay .main .form-sub{
    padding: 20px;
    font-size: 30px;
    width: 100%;
    }
    .info-pay .main .info-transfer .info-bank{
    display:flex;
    flex-wrap: wrap;
    flex-direction: column;
    }
}
@media screen and (max-width: 1200px){
    .info-pay .main .info-transfer .info-bank{
    display:flex;
    flex-wrap: wrap;
    flex-direction: column;
    }
}
::-webkit-scrollbar {
  width: 20px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey; 
  border-radius: 10px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #0071c5; 
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #025a9e; 
}
</style>