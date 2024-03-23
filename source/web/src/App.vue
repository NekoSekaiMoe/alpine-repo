<script setup>
import { ref } from 'vue'
const activityStatus = ref('Pending')
</script>

<template>
  <div>
    <div id="backend">
      <img id="de" src="@/assets/nahida.jpg"/>
      <img id="mo" src="@/assets/nahida-m.jpg"/>
    </div>
    <div id="container">
      <h1>alpine repo homepage</h1>
      <h2>how to use</h2>
      <h3>Work in progress</h3>
      <hr/>
      <p>Powered by <a href="//github.com/dabao1955/" target="_blank">dabao1955</a>. All rights reserved &copy;2018-{{ new Date().getFullYear() }}. Build by <a href="//vitejs.dev/" target="_blank">Vite</a>&nbsp;&&nbsp;<a href="//vuejs.org/" target="_blank">Vue</a></p>
    </div>
  </div>
</template>

<style lang="less">
@font-size: 15px;
// container主元素
// #con {
//   position: fixed;
//   left: 0;
//   right: 0;
//   top: 0;
//   bottom: 0;
// }
#de,#mo {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
}
@media screen and (min-width: 768px) {
  #de {
    display: block;
  }
  #mo {
    display: none;
  }
}
@media screen and (max-width: 768px) {
  #de {
    display: none;
  }
  #mo {
    display: block;
  }
}
#mcimg {
  width: 100%;
}
#container {
  word-break: break-all;
  font-family: 'PingFang SC', '微软雅黑', 'Microsoft Yahei', 'Sogoe UI';
  position: fixed;
  @media screen and (min-width: 768px) {
    left: 50%;
    top: 10%;
    right: 0;
    transform: translate(-50%, -5%);
    bottom: 0;
    overflow-y: auto;
  }
  @media screen and (max-width: 768px) {
    left: 10px;
    right: 10px;
    top: 10px;
    bottom: 10px;
    overflow-y: auto;
    // top:50%;
    // transform: translate(0, -60%);
  }
  border: 1px solid rgba(0,0,0,0,0.8);
  border-radius: 2px;
  padding: 8px;
  box-shadow: 3px 3px 2px 1px rgba(0, 0, 0, 0.2), 1px 2px 3px 3px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
}
// 底层
#container {
  // font size.
  // 不要用 h5 h6!
  h1 {
    font-size: @font-size * 1.8; 
    font-weight: bolder;
  }
  h2 {
    font-size: @font-size * 1.5;
    font-weight: bold;
  }
  h3 {
    font-size: @font-size * 1.3;
    font-weight: bold;
    margin: 2px;
  }
  h4 {
    font-size: @font-size * 1.2;
    font-weight: bold;
  }
  table,table tr th, table tr td {
    border:1px solid #666666;
  }
  table {
    width: 100%;
    border-collapse: collapse;
  }
  a,a:hover,a:active,a:link {
    text-decoration: none;
  }
  a,a:active,a:link {
    color: blue;
  }
  a:hover {
    color:cyan;
  }
  // input select code 必须指定
  p,input,select,span,code,kbd,button,a {
    font-size: @font-size;
  }
  button,input {
    font-size: @font-size * 1.2;
    border-radius: 4px;
    border:1px solid #666666;
    background-color: #ffffff;
    appearance: none;
    -webkit-appearance: none;
  }
  button {
    cursor: pointer;
    a,a:hover,a:active,a:link {
      text-decoration: none;
      color: black;
    }
    a:hover {
      color: black;
    }
  }
  details summary::marker {
    transition: all 10s ease-in-out;
  }
}
</style>
