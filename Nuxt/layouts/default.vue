<template>
    <div>
        <!-- 导航栏 -->
        <div class="header">
            <div class="header-logo">
                <!-- Logo -->
            </div>
            <div class="header-body">
                <ul>
                    <div class="menu">
                        <li class="front-page" bordered><a href="#">首页</a></li>
                        <li class="boiling-point" bordered><a href="#">沸点</a></li>
                        <li class="course" bordered><a href="#" bordered>课程</a></li>
                        <li class="live-streaming" bordered><a href="#">直播</a></li>
                        <li class="activities" bordered><a href="#">活动</a></li>
                        <li class="competitions" bordered><a href="#">竞赛</a></li>
                        <li class="shopping"><a href="#">商城</a></li>
                        <li class="applications"><a href="#">APP</a></li>
                        <li class="plug-in"><a href="#">插件</a></li>
                    </div>
                </ul>
            </div>
        </div>
        <slot />
    </div>
</template>

<style scoped>
*{
    margin: 0;
    padding: 0;
}

li{
    list-style: none;
}
a{
    text-decoration: none;
    color: rgba(0, 0, 0, 0.845);
    padding: 14px 15px;
}
li:first-child a{
    color: rgb(67, 129, 221);
}
.header{
    background-color: white;
    width: 100%;
    height: 50px;
    display: flex;
}
.header .menu{
    display: flex;
    height: 100%;
    line-height: 50px;
    max-width: 100vw;
    padding: 0 20px;
    position: relative;
}
.header .menu li{
    height: 100%;
    box-sizing: border-box;
    position: relative;
}
/* .header li[bordered]:hover{
    color: black;
    border-bottom: 3px solid rgb(47, 67, 223);
} */

.header li[bordered]:hover::after{
    content: "";
    border-bottom: 3px solid rgb(47, 67, 223);
    color: black;
    position: absolute;
    width: 2em;
    bottom: 0;
    left: 26%;
}
.header li:hover a{
    color: black;
}
.header-logo{
    background-image: url("../assets/logo-removebg-preview.png");
    background-size: cover;
    width: 120px;
}
</style>