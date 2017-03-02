<template>
<div class="r_inf">
    <div class="tab-content container col-md-9 col-md-offset-3" >
      <div class="tab-pane fade active" id="mainPage">
        <div class="shade"></div>
        <h2>Welcome to 电子档案管理系统</h2>
      </div>
      <div class="tab-pane fade" id="getInfo">
        <div class="shade"></div>
        <iframe class="frame" src="http://blog.csdn.net/lyr1985/article/details/6067026"></iframe>
      </div>
<!--      <div class="tab-pane fade" id="guiDang">
        <div class="shade"></div>
        <iframe class="frame" src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="chanManage">
         <iframe class="frame" src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="borrowManage">
         <iframe class="frame" src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="destroyManage">
         <iframe class="frame" src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="myInfo">
         <iframe class="frame" src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="Apply">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="Check">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="fileCheck">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="dataCount">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="juese">
        <iframe src="http://baidu.com"></iframe>
      </div>
<!--       <div class="tab-pane fade" id="quanxian">
        <h2>权限管理</h2>
      </div> -->
<!--      <div class="tab-pane fade" id="userManage">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="userGoup">
        <iframe src="http://baidu.com"></iframe>
      </div>
      <div class="tab-pane fade" id="diaryManage">
        <iframe src="http://baidu.com"></iframe>
      </div>  -->
    </div> 
    </div>
</template>

<script>
    export default{
        name: 'r_information',
    }
</script>

<style>
    .r_inf{
        width: 850px;
        height: 900px;
        margin-left: 450px;
        -moz-border-radius: 100px 0 0 100px; 
        -webkit-border-radius: 100px 0 0 100px; 
        border-radius: 100px 0 0 100px;      
        background-color: rgba(111, 84, 153, 1);
      overflow: hidden;
    }

        button {
      border: none;
      padding: 0.6em 1.2em;
      background: rgba(0,0,0,0);
      color: #fff;
      font-family: 'Lato', Calibri, Arial, sans-serif;
      font-size: 1em;
      letter-spacing: 1px;
      text-transform: uppercase;
      cursor: pointer;
      display: block;
      border-radius: 2px;
      line-height: 20px;
      margin-top: 8px;
      display: inline-block;
    }
    button:hover {
      background:rgba(0,0,0,0);
    }
    button:focus,button:visited{
      border:none;
    }
    .navbar{
      margin-bottom: 0;
      /*background: rgba(39,134,180,0.1);*/
      background: rgba(0,0,0,0.7);
      /*box-shadow: 1px 1px 5px rgba(39,134,150,1);*/
     

    }
    .navbar li a{
      text-decoration: none;
      color: #fff;
      cursor:pointer;
    }
    .nav-right{
        line-height: 50px;
        padding: 0; 
        box-sizing:border-box;
        margin-right: 30px;
    }
    .nav-right img{
        width: 40px;
        border-radius: 50%;
    }
    .st-container{
      max-height: 740px;  
      box-sizing:border-box;
      background: rgba(0,0,0,0.7);
      clear: both;
     
    }
    .container{
      left: -40px;
      height: 100%;
      padding: 0;
       -webkit-transition:all 0.6s ;
    }
    .navbar-brand{
      color: #fff;
    }
    #logo{
      font-size: 20px;
      font-weight: 500;
    }
    .secondmenu{
      padding: 0;
      margin: 0;
    }
    .secondmenu li{
      background: rgba(85,155,180,0.1);
    }
    .welcomePage{
      color: #fff;
      margin-left: 50px;
    }
    .panel{
      border:none;
      background:none;
    }
    .panel-group{
      margin: 0;
      padding: 0;
    }
    .panel-heading{
      background: rgba(39,134,180,0.1);
      position: relative;
      width: 100%; 
      display: inline-block;
      border: none;
    }
    .panel-title{
      background: rgba(39,134,180,0.1);
      display:inline;
      height: 100%;
      color: #fff;
    }
     .panel-title a{
      width: 100%;
      text-decoration: none;
     }
    .panel-body {
      background: rgba(39,134,180,0.1);
      padding: 0;
      margin: 0;
    }
    .tab-pane{
      height: 100%;
      color: #fff;
    }
    .right{
      left: 120px;
    }
    iframe{
      border: none;
      height: 100%;
      width: 100%;
    }
    .shade{
      position: absolute;
      height: 100%;
      width: 100%;
      display: none;
    }
</style>