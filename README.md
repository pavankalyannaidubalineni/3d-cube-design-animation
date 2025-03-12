<!DOCTYPE html>
<html lang="zh-ch">

<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=div, initial-scale=1.0">
	<meta name="title" content="3D Cube - For Crush | Aoudumber Bade">
    <meta name="github" content="https://github.com/Balineni Pavan Kalyan">
	<link rel="stylesheet" href="./css/program.css">
	<title>3D Cube - For mine | pavan kalyan</title>
       <style>* {
        margin: 0px;
        padding: 0px;
    }
    
    html {
        overflow: hidden;
        height: 100%;
        background: linear-gradient(rgb(245 69 69 / 77%), rgb(255 39 205 / 84%)), url(../images/background.jpg);
    }
    
    body {
        width: 100vw;
        height: 95vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 9px;
    }
    
    .title {
        color: rgb(238, 255, 255);
        text-align: center;
        text-shadow: /* 0px 1px 0px #999, 0px 2px 0px #888, 0px 3px 0px #777, 0px 4px 0px #666, 0px 5px 0px #555, 0px 6px 0px #444, 0px 7px 0px #333, 0px 8px 7px #001135 */;
        font-size: 2.2rem;
        font-weight: 800;
        letter-spacing: 11px;
        margin-top: -87px !important;
        text-transform: uppercase;
        /* justify-self: flex-start; */
    }
    
    .cube {
        position: relative;
        margin: 0px auto;
        margin-top: 15%;
        /* margin-left: 42%; */
        width: 200px;
        height: 200px;
        transform: rotateX(-30deg) rotateY(-85deg);
        transform-style: preserve-3d;
        animation: rotate 15s infinite;
    }
    
    .cube .outer-cube,
    .cube .inner-cube {
        transform-style: preserve-3d;
    }
    
    /* 旋转立方体 */
    @keyframes rotate {
        from {
            transform: rotateX(0deg) rotateY(0deg);
        }
    
        to {
            transform: rotateX(360deg) rotateY(360deg);
        }
    }
    
    /* 外层立方体样式 */
    .outer-cube .outer-top,
    .outer-cube .outer-bottom,
    .outer-cube .outer-right,
    .outer-cube .outer-left,
    .outer-cube .outer-front,
    .outer-cube .outer-back {
        position: absolute;
        top: 0;
        left: 0;
        width: 180px;
        height: 200px;
        border: 1px solid #fff;
        opacity: 0.3;
        transition: all .10s;
        background-size: cover;  /* Ensures the image covers the full area */
        background-position: center; /* Centers the image */
        background-repeat: no-repeat;
    }
    
    .outer-cube img {
        width: 100%;
        height: 210px;
        object-fit: cover; /* Ensures the image fills the container without stretching */
        
    }
    
    
    .outer-top {
        transform: rotateX(90deg) translateZ(100px);
    }
    
    .outer-bottom {
        transform: rotateX(-90deg) translateZ(100px);
    }
    
    .outer-front {
        transform: rotateY(0deg) translateZ(100px);
    }
    
    .outer-back {
        transform: translateZ(-100px) rotateY(180deg);
    }
    
    .outer-left {
        transform: rotateY(90deg) translateZ(100px);
    }
    
    .outer-right {
        transform: rotateY(-90deg) translateZ(100px);
    }
    
    /* 嵌套的内层立方体样式 */
    .inner-cube>div {
        position: absolute;
        top: 35px;
        left: 35px;
        width: 130px;
        height: 130px;
    }
    
    .inner-cube img {
        width: 130px;
        height: 130px;
    }
    
    .inner-top {
        transform: rotateX(90deg) translateZ(65px);
    }
    
    .inner-bottom {
        transform: rotateX(-90deg) translateZ(65px);
    }
    
    .inner-front {
        transform: rotateY(0deg) translateZ(65px);
    }
    
    .inner-back {
        transform: translateZ(-65px) rotateY(180deg);
    }
    
    .inner-left {
        transform: rotateY(90deg) translateZ(65px);
    }
    
    .inner-right {
        transform: rotateY(-90deg) translateZ(65px);
    }
    
    .cube:hover .outer-top {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: rotateX(90deg) translateZ(200px);
    }
    
    .cube:hover .outer-bottom {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: rotateX(-90deg) translateZ(200px);
    }
    
    .cube:hover .outer-front {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: rotateY(0deg) translateZ(200px);
    }
    
    .cube:hover .outer-back {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: translateZ(-200px) rotateY(180deg);
    }
    
    #copy {
        position: fixed;
        bottom: 12px;
        left: 50%;
        transform: translateX(-50%);
        font-size: 1rem;
    }
    
    #copy a {
        text-decoration: none;
        color: #191919d7;
    }
    
        #copy p {
        color: #fff6f9;
        text-align: center;
        font-weight: 700;
        cursor: pointer;
        }
    
    
    .cube:hover .outer-left {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: rotateY(90deg) translateZ(200px);
    }
    
    .cube:hover .outer-right {
        right: -70px;
        bottom: -70px;
        opacity: 0.8;
        transform: rotateY(-90deg) translateZ(200px);
    }
    
    .message .author {
        position: absolute;
        right: 50px;
        background-image: -webkit-linear-gradient(left, blue, #66ffff 10%, #cc00ff 20%, #CC00CC 30%, #CCCCFF 40%, #00FFFF 50%, #CCCCFF 60%, #CC00CC 70%, #CC00FF 80%, #66FFFF 90%, blue 100%);
        font-size: 35px;
        -webkit-text-fill-color: transparent;
        -webkit-background-clip: text;
        -webkit-background-size: 200% 100%;
        -webkit-animation: masked-animation 4s linear infinite;
    }
    
    @keyframes masked-animation {
        0% {
            background-position: 0 0;
        }
    
        100% {
            background-position: -100% 0;
        }
    }
    
    .message .tip {
        position: absolute;
        /* right: 10px; */
        left: 50%;
        transform: translateX(-50%);
        bottom: 30px;
        margin-top: 60px;
        color: white;
        font-size: 18px;
    }
</style>
</head>

<body>
	<div class="title">
		pavan kalayn 💗
	</div>

	<div class="cube">
		
		<div class="outer-cube">
			<div class="outer-top">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\stylish.jpg" />
			</div>
			<div class="outer-bottom">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\front view.jpg" />
			</div>
			<div class="outer-front">
				
                <img src="c:\Users\Devendra Naidu GK\Desktop\gate\blue t shirt.jpg" />
			</div>
			<div class="outer-back">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\side view.jpg" />
			</div>
			<div class="outer-left">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\bike.jpg" />
			</div>
			<div class="outer-right">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\diploma.jpg">
		</div>
		<!-- 内层立方体 -->
		<div class="inner-cube">
            <div class="inner-top">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\stylish.jpg" />
			</div>
			<div class="inner-bottom">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\front view.jpg" />
			</div>
			<div class="inner-front">
				
                <img src="c:\Users\Devendra Naidu GK\Desktop\gate\blue t shirt.jpg" />
			</div>
			<div class="inner-back">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\side view.jpg" />
			</div>
			<div class="inner-left">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\bike.jpg" />
			</div>
			<div class="inner-right">
				<img src="c:\Users\Devendra Naidu GK\Desktop\gate\diploma.jpg">
		</div>
			
		</div>
	</div>
	<div>
		<div class="message">
			<div class="tip">
				<!-- Tip: Move the mouse in and out of the cube and the effect will be displayed! -->
			</div>
		</div>
	</div>

	<div id="copy">
		<p class="text-center text-white text-sm">pk Creator <a
			href="https://www.instagram.com/pavan_k_n_b/reels/#">@pavank.shar</a></p>
	  </div>
</body>

</html>
