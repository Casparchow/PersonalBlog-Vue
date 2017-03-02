<template>
<div class="nav-main">
  <div class="nav-box">
    <div class="nav">
      <ul class="nav-ul">
  	    <li><a href="#" class="home"><span>首页</span></a></li>
  	    <li><a href="#" class="develop"><span>H5开发</span></a></li>
  	    <li><a href="#" class="wechat"><span>微信推广</span></a></li>
  	    <li><a href="#" class="case"><span>项目案例</span></a></li>
  	    <li><a href="#" class="news"><span>信息资讯</span></a></li>
  	    <li><a href="#" class="contact"><span>关于我们</span></a></li>
      </ul>
    </div>
  <div class="nav-slide">
      <div class="nav-slide-o"></div>
      <div class="nav-slide-o">
    	  <ul>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    		  <li><a href="#"><span>微信开发</span></a></li>
    	  </ul>
      </div>
      <div class="nav-slide-o">
    	  <ul>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    		  <li><a href="#"><span>微信关注</span></a></li>
    	  </ul>
      </div>
      <div class="nav-slide-o">
    	  <ul>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    		  <li><a href="#"><span>网站设计</span></a></li>
    	  </ul>
      </div>
      <div class="nav-slide-o">
    	  <ul>
    	  	<li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    		  <li><a href="#"><span>企业建站</span></a></li>
    	  </ul>
      </div>
    </div>
  </div>
</div>
</template>


<script type="text/javascript" src="../assets/js/jquery-1.9.1.min.js"></script>
<script>
import r_inf from '../components/r_information.vue' 

export default {
  name: 'l_nav',
  data () {
    return {

    }
  },
  components: {
    r_inf 
  },
}

//导航栏
$(function(){
	var thisTime;
	$('.nav-ul li').mouseleave(function(even){
			thisTime	=	setTimeout(thisMouseOut,1000);
	})

	$('.nav-ul li').mouseenter(function(){
		clearTimeout(thisTime);
		var thisUB	=	$('.nav-ul li').index($(this));
		if($.trim($('.nav-slide-o').eq(thisUB).html()) != "")
		{
			$('.nav-slide').addClass('hover');
			$('.nav-slide-o').hide();
			$('.nav-slide-o').eq(thisUB).show();
		}
		else{
			$('.nav-slide').removeClass('hover');
		}
		
	})
	
	function thisMouseOut(){
		$('.nav-slide').removeClass('hover');
	}
	 
	$('.nav-slide').mouseenter(function(){
		clearTimeout(thisTime);
		$('.nav-slide').addClass('hover');
	})
	$('.nav-slide').mouseleave(function(){
		$('.nav-slide').removeClass('hover');
	})

})
</script>


<style scoped>
ol, ul, li { list-style: none; line-height: 22px; }
ol, ul { zoom: 1; }
h1, h2, h3, h4, h5, h6 { font-size: 100%; }
img { border: none; max-width: 100%; }
a, a:link, a:visited { cursor: pointer; text-decoration: none;}
a:hover { cursor: pointer; }
.table { border-collapse: collapse; border-spacing: 0; }
    .table td { border: solid 1px #666; }
.clear { clear: both; float: none; overflow: hidden; height: 0; font-size: 0; }
.clearFix:after { clear: both; display: block; visibility: hidden; height: 0; line-height: 0; content: "."; }
.clearFix { zoom: 1; }
* { -webkit-box-sizing: border-box; -moz-box-sizing: border-box; box-sizing: border-box; }
:after, :before { -webkit-box-sizing: border-box; -moz-box-sizing: border-box; box-sizing: border-box; }

.font { font: 14px/24px "Comic Sans MS"; }
:focus { outline: none; }

/*一级导航*/
.nav-main{
	position: fixed;
	top: 0;
	z-index: 12;
	height: 100%;
	width: 100px;
	color: #fff;
	background: rgba(44, 62, 80, 1);
}
.nav-main a{color: #fff;}
.nav-box{
	position: relative;
	perspective: 200px;
	-webkit-perspective: 200px;
	transform-style: preserve-3d;
	-webkit-transform-style: preserve-3d;
	height: 100%;
	z-index: 99;
}
.nav-ul li a{
	display: block;
	width: 100px;
	height: 100px;
	overflow: hidden;
	text-align: center;
	position: relative;
	transition: all .5s;
	-moz-transition: all .5s;
	-webkit-transition: all .5s;
	-o-transition: all .5s;
}
.nav-ul li a:before{
	content: '';
	position: absolute;
	left: -240px;
	top: 0px;
	width: 200px;
	height: 100%;
	background: rgba(111, 84, 153, 1);
	z-index: 1;
	transform: skew(30deg, 0);
	-webkit-transform: skew(30deg, 0);
	-ms-transform: skew(30deg, 0);
	-moz-transform: skew(30deg, 0);
	-o-transform: skew(30deg, 0);
	transition: all .5s;
	-moz-transition: all .5s;
	-webkit-transition: all .5s;
	-o-transition: all .5s;
}
.nav-ul li a:hover{background: rgba(133, 84, 165, 1);}
.nav-ul li a:hover:before{left: -30px;}
.nav-ul li a:after{
	content: '';
	position: absolute;
	width: 100%;
	height: 30px;
	left: 0;
	top: 20px;
	z-index: 1;
}
.nav-ul li a span{
	display: block;
	margin-top: 60px;
	position: relative;
	z-index: 1;
}


.nav-slide{
	position: fixed;
	left: 100px;
	top: 0;
	width: 240px;
	height: 100%;
	background: rgba(35, 49, 64, 1);
	transform: rotateY(120deg);
	-webkit-transform: rotateY(120deg);
	-moz-transform: rotateY(120deg);
	-o-transform: rotateY(120deg);
	-ms-transform: rotateY(120deg);
	z-index: 99;
	visibility: hidden;
	transform-origin: 0 0;
	-webkit-transform-origin: 0 0;
	-moz-transform-origin: 0 0;
	-o-transform-origin: 0 0;
	-ms-transform-origin: 0 0;
	backface-visibility: hidden;
	-webkit-backface-visibility: hidden;
	transition: all .5s;
	-webkit-transition: all .5s;
	-moz-transition: all .5s;
	-o-transition: all .5s;
	transition-timing-function: cubic-bezier(.08, .72, .71, .96);
	-webkit-transition-timing-function: cubic-bezier(.08, .72, .71, .96);
}
.nav-slide.hover{
	transform: rotateY(0deg);
	-webkit-transform: rotateY(0deg);
	-moz-transform: rotateY(0deg);
	-o-transform: rotateY(0deg);
	-ms-transform: rotateY(0deg);
	z-index: 15;
	visibility: visible;
}

/*二级菜单*/
.nav-slide-o li a{
	line-height: 50px;
	display: block;
	padding: 0 20px;
	font-size: 14px;
	overflow: hidden;
	text-align: left;
	position: relative;
	transition: all .5s;
	-webkit-transition: all .5s;
	-moz-transition: all .5s;
	-o-transition: all .5s;
}
.nav-slide-o li a:before{
	content: '';
	position: absolute;
	left: -230%;
	top: 0px;
	width: 200%;
	height: 100%;
	background: rgba(111, 84, 153, 1);
	z-index: 1;
	transform: skew(30deg, 0);
	-webkit-transform: skew(30deg, 0);
	-moz-transform: skew(30deg, 0);
	-o-transform: skew(30deg, 0);
	-ms-transform: skew(30deg, 0);
	transition: all .5s;
	-webkit-transition: all .5s;
	-moz-transition: all .5s;
	-o-transition: all .5s;
}
.nav-slide-o li a:hover{background: rgba(133, 84, 165, 1);}
.nav-slide-o li a:hover:before{left: -60px;}
.nav-slide-o li a span{position: relative;z-index: 1;}
.nav-slide-o {display: none;}

</style>
