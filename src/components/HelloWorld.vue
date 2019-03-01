<template>
  <div class="hello">
    {{ msg }}
    <div class="box ignore">Essential Links</div>
    <div aspectratio>
      <div aspectratio-content>
        <div w-188-246>w-188-246</div>
      </div>
    </div>
    <div class="example">example111</div>
    <div id="example">example222</div>

    <div class="aspectration example" data-ratio="16:9">
      <div class="content"></div>
    </div>
    <div class="aspectration example" style="--aspect-ratio:1.4">
      <div class="content"></div>
    </div>
    <div class="aspectration1 example" data-ratio="16:9">
      <div class="content"></div>
    </div>
    <div class="aspect-ratio-boxes"></div>

    <div class="aspect-ratio-box">
      <iframe class="aspect-ratio-box-inside" src="https://www.youtube.com/embed/upPCohrJcbw?showinfo=0&modestbranding=1" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="aspect-ratio-box1">
      很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。很显然溢出容器的内容被裁切掉了。这个时候较好的解决方案就是把overflow:hidden换成overflow:auto。但也是美中不足，会出现滚动条。
    </div>
    <div class="last-aspect-ratio" style="--aspect-ratio:1.95;"></div>
    <div class="last-aspect-ratio" style="--aspect-ratio:1.78;"></div>
    <div class="last-aspect-ratio" style="--aspect-ratio:1.4;"></div>
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
*{
  margin:0;
  padding: 0;
  border:0;
}
body{
  width:100%;
}
.hello{
  border: .5px solid black;
  border-bottom-width: 4px;
  font-size: 14px;
  line-height: 28px;
  position: relative;
}
.ignore{
  margin: 10px;
  background-color: red;
}
.box{
  width:180px;
  height:300px;
}
.hairlines{
  border-bottom: 0.5px solid red;
}
[aspectratio] {
  position: relative;
  }
[aspectratio]::before {
  content: '';
  display: block;
  width: 1px;
  margin-left: -1px;
  height: 0;
}
[aspectratio-content] {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
}
[w-188-246]{
  width:188px;
  background-color:red;}
[w-188-246]{
  aspect-ratio:'188:246';
}
/* 实现1px */
@svg 1px-border{
  height: 2px;
  @rect{
    fill:var(--color, black);
    width: 100%;
    height:50%;
  }
}
.example{
  border: 1px solid transparent;
  border-image: svg(1px-border param(--color #00b1ff)) 2 2 stretch;
}
@svg square{
  @rect{
    fill:var(--color,black);
    width: 100%;
    height:100%;
  }
}
#example{
  margin:10px;
  background: white svg(square param (--color #00b1ff));
}

/* 垂直方向的padding */
.aspectration{
  position: relative;
  height:0;
  width:100%;
  background-color: orange;
}
.aspectration[data-ratio="16:9"]{
  /* padding-top: 56.25%; */
  padding-top:calc(100% * 9 / 16);
}
.aspectration[data-ratio="4:3"]{
  padding-top:75%;
}
/* padding&css */
.aspectration[style*="--aspect-ratio"] {
    padding-top: calc(100% / (var(--aspect-ratio)))
  }
.aspectration > *{
  position: absolute;
  left:0;
  top:0;
  width:100%;
  height: 100%;
}

.aspectration1{
  display: grid;
  grid-template-columns: repeat(16, 6.25vw);
  grid-auto-rows: 6.25vw;
}
.aspectration1[data-ratio="16:9"] .content{
  grid-column: span 16;
  grid-row: span 9;
}
.aspect-ratio-boxes{
  overflow: hidden;
  height: 0;
  padding-top:56.25%;
  background:url(/images/happy-birthday.svg);
}

.aspect-ratio-box {
  height: 0;
overflow: hidden;
padding-top: calc((591.44 / 1127.34) * 100%);
background: white;
position: relative;
}
.aspect-ratio-box-inside {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  }
  .aspect-ratio-box1 { background: white; }
  .aspect-ratio-box1::before { content: "";
  width: 1px;
  margin-left: -1px;
  float: left;
  height: 0;
  padding-top: calc(591.44 / 1127.34 * 100%);
  }
  .aspect-ratio-box1::after {
    /* to clear float */
  content: "";
  display: table;
  clear: both;
  }

  /* :root { --aspect-ratio: 1 / 1; } */
  [style*="--aspect-ratio"]{
      width: 50vw;
    margin: 20px auto;
    background:orange; }
  [style*="--aspect-ratio"] > :first-child
  { width: 100%; }
  [style*="--aspect-ratio"] > *
  { height: auto; }
  @supports (--custom:property)
  {
    [style*="--aspect-ratio"] {
      position: relative;
    }
    [style*="--aspect-ratio"]::before {
    content: "";
    display: block;
    padding-bottom: calc(100% / (var(--aspect-ratio)));
    }
    [style*="--aspect-ratio"] > :first-child {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      }
    }

</style>
