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
<style scoped>
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
</style>
