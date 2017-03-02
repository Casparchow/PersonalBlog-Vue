<template>
    <div id="bod" class="electro"></div>
</template>

<script>
    export default {
        name: 'electrocardiogram'
    }
    ;$(function() {
        var bod = document.querySelector('#bod');

        bod.appendChild(createCircle(400, 15));
        
        var cur_x = 400;//初始水平坐标
        var cur_y = 15;//初始垂直坐标
        var unit_x = 1;//固定水平单元距离
        var unit_y = 30;//最大垂直单元距离
        var angle = 0;//角度
        var dis = 0;//随机水平距离
        var point_x = cur_x+dis;//目标位置

        var canDraw = true;//是否可画

        setInterval(function() {
            canDraw = false;
            if(cur_x >= point_x) {//开始下一个随机点
                console.log(cur_y);
                angle = Math.round(Math.random()*2);
                switch(angle) {
                    case 0://上
                        angle=10;
                        break;
                    case 1://水平
                        angle=0;
                        break;
                    case 2://下
                        angle=-10;
                        break;
                }
                dis = Math.round(Math.random()*10+10);
                point_x = cur_x+dis;
            }else {
                switch(angle) {
                    case 10://上
                        if(cur_x < point_x-dis/2) {
                            cur_y -= parseInt((dis - (point_x-cur_x))*Math.tan(angle*Math.PI/180));
                        }else {
                            cur_y += parseInt(((point_x-cur_x))*Math.tan(angle*Math.PI/180));
                        }
                        bod.appendChild(createCircle(cur_x, cur_y));
                        cur_x += 0.5;
                        break;
                    case 0://水平
                        bod.appendChild(createCircle(cur_x, cur_y));
                        cur_x += 3;
                        break;
                    case -10://下
                        if(cur_x < point_x-dis/2) {
                            cur_y -= parseInt((dis - (point_x-cur_x))*Math.tan(angle*Math.PI/180));
                        }else {
                            cur_y += parseInt(((point_x-cur_x))*Math.tan(angle*Math.PI/180));
                        }
                        bod.appendChild(createCircle(cur_x, cur_y));
                        cur_x += 0.5;
                        break;
                }
            }
//            while(cur_x>1200){
//                clearInterval();
//            }
        }, 3);

        function createCircle(x, y) {
            var circle = document.createElement('bod');
            circle.setAttribute('class', 'circle');
            circle.style.left = x +'px';
            circle.style.top = y +'px';
            return circle;
        }
    });
</script>

<style>
    .electro{
        width:1200px;
        height: 30px;
        position: relative;
    }
    .circle{
        background: white;
        width: 2px;
        height: 2px;
        border-radius: 100px;
        position: absolute;
    }
</style>