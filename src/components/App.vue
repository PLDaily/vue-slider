<style type="text/css">
*{
	padding: 0;
	margin: 0;
}
</style>
<template>
<div id="main">
	<slider :pages="slider_data" :sliderinit="sliderinit">
    </slider>
</div>
</template>
<script>
import Slider from './Slider.vue'
export default {
	components: {slider: Slider},
	data() {
		var sliderinit = {
            width: 710,
            height: 320,
            imgCount: 7,
            dots: true,//是否显示轮番点
            button: true,//是否显示前进后退按钮
            currentPage: 0,//起始页
            changeTime: 5000,//时间间隔
            animateTime: 1000,
            autoplay:true//自动播放
        };
        var slider_data = [
	        {
	        	title: "Colosseo (Colosseum), ca. 75 AD",
	        	src: "../img/feature-colosseo.jpg"
	        },
	        {
	        	title: "Fontana di Trevi (Trevi Fountain), 1762",
	        	src: "../img/feature-trevi.jpg"
	        },
	        {
	        	title: "Arco di Constantino (Arch of Constantine), 315 AD",
	        	src: "../img/feature-arch.jpg"
	        },
	        {
	        	title: "Santa Maria Maggiore",
	        	src: "../img/feature-santamaria.jpg"
	        },
	        {
	        	title: "Colonna Traiana (Trajan’s Column), 113 AD",
	        	src: "../img/feature-trajan.jpg"
	        },
	        {
	        	title: "Il Vittoriano, 1911",
	        	src: "../img/feature-vittoriano.jpg"
	        },
	        {
	        	title: "Locks near Trevi Fountain",
	        	src: "../img/feature-locks.jpg"
	        }
	    ];
	    return {
	    	sliderinit: sliderinit,
	    	slider_data: slider_data
	    }
	}
}	
</script>