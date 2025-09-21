<template>
    <div>
        图片
        <img id="tt" src="../../public/bg.png" alt="本地图片" >
         <p class="quote">这是一段引用文本</p>
<!-- 渲染后效果："这是一段引用文本"（引号为红色） -->
    </div>

</template>
<style>
/* 在 .quote 元素内容前添加左引号，内容后添加右引号 */
#tt {
  width: 200px;
  height: 100px;
  padding: 10px;
  border: 5px solid #000;
  margin: 5px #f00;
  /* 标准盒模型下：
     总宽度 = 200 + 10*2 + 5*2 = 230px
     总高度 = 100 + 10*2 + 5*2 = 130px */
}
</style>