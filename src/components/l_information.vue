<template>
    <div class="l_inf">
        <!--个人信息-->
        <div class="per_inf">
            <a style="  text-decoration: none;color:white" href="http://baidu.com"><img class="head_portrait" src="../assets/image/Head_portrait.jpg"><h3>Caspar Chow</h3></a>
            
            <div class="">
                <ul>
                    <li  v-html="item.lable" v-for="item in items_t" class="list_per"></li>
                </ul>
            </div>
        </div>

        <!--常访链接-->
        <div class="url_inf">
            <h3>常访链接</h3>
            <div class="message">
                <ul>
                    <li  v-html="item.lable" v-for="item in items_l" class="list_url"></li>
                </ul>
            </div>
            <div class="message">
                <ul>
                    <li  v-html="item.lable" v-for="item in items_r" class="list_url"></li>
                </ul>
            </div>
        </div>

        <!--Web前端相关信息-->
        <div class="web_inf"></div>

    </div>
</template>
<script>

    export default{
        name: 'l_information',
        data() {
            return {
                items_t:[
                    {
                        lable: '电话：13538811074'
                    },
                    {
                        lable: '地址：China'
                    },
                    {
                        lable: '邮箱：1393978611@qq.com'
                    },
                    {
                        lable: '兴趣：篮球 设计'
                    }
                ],
                items_l:[
                    {
                        lable: '百度',
                    },
                    {
                        lable: '谷歌'

                    },
                    {
                        lable: '搜狗'
                    }
                ],
                items_r:[
                    {
                        lable: '慕课网',
                    },
                    {
                        lable: '极客网',
                    },
                    {
                        lable: 'vue.js',
                    }
                ]

            }
        }
    }
</script>
<style>
    .l_inf{
        width: 300px;
        height: 900px;
        margin-left: 100px;
        -moz-border-radius: 0 100px 100px 0; 
        -webkit-border-radius: 0 100px 100px 0;
        border-radius: 0 100px 100px 0;
        float: left;
        background-color: rgba(111, 84, 153, 1);
        position: relative;
    }

    /*个人信息*/    
    .per_inf{
        width: 300px;
        height: 350px;
/*        background-color: rgba(63, 135, 141, 0.1);*/
        text-align: center;
        color: white;
    }
    .head_portrait{
        width: 150px;
        height: 150px;
        margin-top: 20px;
        -moz-border-radius: 75px;
        -webkit-border-radius: 75px;
        border-radius: 75px;
    }
    .list_per{
        list-style: none;
        margin: 10px 0 10px 60px;
        text-align: left;
        font-size: 14px;
    }
    .per_inf h3{
        padding: 0;
        margin: 0 0 30px 0;
    }
        
    /*常访链接*/ 
    .url_inf{
        width: 200px;
        height: 200px;
        padding: 0 20px 0 20px;
        position: absolute;
        top: 350px;
        left: 30px;
        -moz-border-radius: 15px;
        -webkit-border-radius: 15px;
        border-radius: 15px;
/*        box-shadow: 0 0 100px #7e0766 inset; 
        background-color: rgba(108, 103, 110, 1);*/
        background-color: white;
        color: black;  
    }
    .url_inf h3{
        padding: 0;
        margin: 10px 0 3px 0;
        text-align: center;
        font-size: 25px;
        height: 25px;
    }
    .message{
        width: 100px;
        border-top: 5px  groove rgba(63, 51, 65, 0.5); 
        float: left;
    }
    ul{
        padding: 0;
        margin: 0;
    }
    .list_url{
        list-style: none;
        margin: 25px 0 20px 0;
        text-align: center;
    }

    /*Web前端相关信息*/ 
    .web_inf{
        width: 200px;
        height: 295px;
        padding: 0 20px;
        position: absolute;
        top: 575px;
        left: 30px;
        -moz-border-radius: 15px 15px 75px 15px;
        -webkit-border-radius: 15px 15px 75px 15px;
        border-radius: 15px 15px 75px 15px;
/*        box-shadow: 0 0 100px #7e0766 inset;
        background-color: rgba(108, 103, 110, 1); */
        background-color: rgba(255, 255, 255, 1);
    }
</style>