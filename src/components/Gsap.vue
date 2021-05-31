<template>
  <div id='logo'>你好李焕英</div>
<!-- <div class='stagger'></div>
<div class='stagger'></div>
<div class='stagger'></div>
<div class='stagger'></div> -->

<!-- <svg viewBox='0 0 1200 600' style="background:yellow">
  <rect id='r1' x='50' y='100' width='100' height='100' />
  <rect id='r2' x='350' y='100' width='100' height='100' />
</svg> -->
</template>
<script>
import gsap from 'gsap'
import { MotionPathPlugin } from "gsap/all";
gsap.registerPlugin(MotionPathPlugin)

export default {
  name: 'Gsap',
  mounted(){
    // 平滑移动到右边x坐标100px的位置，持续过程1s

    // 曲线运动
    gsap.to('#logo',{duration: 4, motionPath: {
        path: [{x:0, y:0}, {x:500, y:0}, {x:0, y:200}, {x:500, y:500}, {x: 0, y: 0}]
    }})

    // 贝塞尔曲线运动
    // gsap.to('#logo',{duration: 3, motionPath: {
    //     path: [{x:0, y:0}, {x:500, y:0}, {x:0, y:200}, {x:500, y:500}],
    //     type: 'cubic'
    // }})

    // gsap.to不仅可以操作dom，还可以操作js对象
    // var obj = {prop: 10};
    // gsap.to(obj, {
    //   duration: 1,
    //   prop: 200, 
    //   //onUpdate fires each time the tween updates; we'll explain callbacks later.
    //   onUpdate: function() {
    //     console.log(obj.prop); //logs the value on each update.
    //   }
    // });

    // 沿着x轴旋转360°
    // gsap.to('#logo',{duration: 3, rotationX: 360, repeat: 1})
    // gsap.to('#logo',{duration: 3, rotationY: 360})
    // gsap.to('#logo',{duration: 3, x: 100, y: 100, scale: 2, skewX: 45, rotation: 180})

    // 按照元素宽度的百分比沿x轴移动
    // gsap.to('#logo',{duration: 3, xPercent: 1000})
    // 按照元素宽度的百分比沿y轴移动
    // gsap.to('#logo',{duration: 3, yPercent: 1000})

    // 放大元素的n倍
    // gsap.to('#logo',{duration: 3, scale: 30})
    // gsap.to('#logo',{duration: 3, scaleX: 30})
    // gsap.to('#logo',{duration: 3, scaleY: 30})
    //歪曲45度
    // gsap.to('#logo',{duration: 3, skewX: 45})
    // gsap.to('#logo',{duration: 3, skewY: 45})
    // gsap.to('#logo',{duration: 3, rotation: 360})
    // gsap.to('#logo',{duration: 3, rotationX: 360})
    // gsap.to('#logo',{duration: 3, rotationY: 360})

    // from tweens
    // gsap.from('#logo',{duration: 2, x: 500, scale: 0.5, opacity: 0})

    // fromTo tweens
    // gsap.fromTo('#logo',{width: 0, height: 0}, {duration: 1.5, width: 100, height: 200})

    // 设置属性，相当于duration为0的补间动画
    // gsap.set('#logo', {fontSize: 20, x: 10})

    // ease取值范围：none,power1,power2,power3,power4,back,elastic,bounce,rough,slow,steps,circ,expo,sine,custom
    // type:in,out,inOut
    // gsap.to('#logo',{duration: 2, ease: `sine`, x: 500})

    // gsap.to('.stagger',{duration: 1, stagger: 1, x: 300}).to('.stagger', {duration: 1, stagger: 1, x: 0})

    // 10分钟搞定网页动画|gsap教程
    // gsap.set('#r1', {transformOrigin: 'center'})
    // gsap.set('#r2', {transformOrigin: 'center'})
    // let t1 = gsap.timeline() // 时间线实例用于编排多个动画的执行顺序
    // t1.to('#r1', {
    //   duration: 1,
    //   x: 100, 
    //   scaleX: 2,
    //   fill: 'red',
    //   stroke: 'white',
    //   rotation: 360,
    //   strokeWidth: 5,
    //   // repeat: -1, // -1是重复无限次
    //   yoyo: true // 类似悠悠球一样的镜像运动，即运动完了之后再反向运动回来
    //   }).from('#r2', {
    //   duration: 1,
    //   x: 100, 
    //   scaleX: 2,
    //   fill: 'red',
    //   stroke: 'white',
    //   rotation: 360,
    //   strokeWidth: 5,
    //   // repeat: -1, // -1是重复无限次
    //   yoyo: true // 类似悠悠球一样的镜像运动，即运动完了之后再反向运动回来
    //   }, '>-0.5') // 第三个参数中：>代表上一个动画结束时间点，<代表上一个动画开始的时间点，在这里表示上一个动画结束时间点往前推0.5s就执行第二个动画
  
  }
}
</script>
<style scoped>
#logo {
  width:100px;
  height:100px;
  background-color:red;
}
.stagger {
  width:100px;
  height:100px;
  background-color:red;
}
</style>