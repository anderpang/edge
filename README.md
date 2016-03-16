 <h3>自创自用前端利器</h3>

  <b>环境</b>：<br />
  Java+Nodejs+window系统（未测其他系统）<br />
  <b>功能</b>：<br />
  1、css编写，不用写前缀，保存后自动加-webkit-、-moz-、-o-前缀，并压缩文件。<br />
  现支持的、不加前缀的css属性有：transform、transition、animation、@keyframes、user-select、linear-gradient、radial-gradient。<br />
  2、js保存后自动压缩。<br />
  3、源码中创建文件夹、保存文件，压缩路径中自动生成。<br />
  4、配置简单。<br />
 <b>使用</b>:<br />
 1、配置Java环境及Nodejs环境，方法网上自行搜索。<br />
 2、下载本edge代码（方式随意），放任一路径内。<br />
 比如我就放在F:\web中：<br />
 <img src="images/article/1458100529295/1.jpg" alt="" />
 3、假设我有一web站点,src文件夹为放源文件的地方（可随意命名）：<br />
 <img src="images/article/1458100529295/2.jpg" alt="" />
 4、edge/config.js文件中配置源码路径(可用相对路径，不同盘符也是可以的。只用过utf8编码，其他编码未测试。因本人一直都用utf8，呵呵）：<br />
 <img src="images/article/1458100529295/3.jpg" alt="" />
 5、启用Nodejs command prompt命令行，转到edge目录下。<br />
   输入npm start启动程序,看到Listening就表示启动成功了！<br />
   <img src="images/article/1458100529295/4.jpg" alt="" />
   接下来就可以开始搬砖了。。。<br />
   -----------------------------------------------
 6、到website/src/css中建一style.css测试文件。(假如测试代码如下）<br />
 <img src="images/article/1458100529295/5.jpg" alt="" /><br />
 保存文件后，website中已经生成css目录及style.css文件。<br />
 <img src="images/article/1458100529295/6.jpg" alt="" />
 <img src="images/article/1458100529295/7.jpg" alt="" />
 7、js文件同css...<br />
 <hr />
 <p><b>自问自答</b></p>
 <p>
    <b>Q</b>：为什么要弄这工具？<br />
    &emsp;&emsp;<b>A</b>：css和js写多了，老要进行各种处理，比如css的前缀啊，写得就烦人，也影响速度，写完后还得压缩，虽然网上也有自动压缩的方法，但都不太满意。用sass写css吧，那种非标准的@include语法，会觉得不太好，还是写正统的css比较放心，而且在没安装sass下，用标准浏览也能看纯正的css效果。
 </p>
 <p>
    <b>Q</b>：为什么没有在同目录下生成filename-min.js文件？<br />
    &emsp;&emsp;<b>A</b>：这个可以实现，比现在的还容易，稍微改下源码就可以了。之所以不弄成那样原因有两：1、仿java的源码；2、个人在长期的积累下，觉得源码和压缩的文件放一起，以后想清理时就很混乱，还得一个个对比，不敢乱删。现在分手放，就可以放心的直接删除压缩的目录了。
 </p>
 <p>
    <b>Q</b>：css想加新属性怎么处理？<br />
    &emsp;&emsp;<b>A</b>：在adge/lib/cssRule.js中增删相应规则即可，但要会点js才行哦。
 </p>
 Over！<br />
 自用程序，可能有不尽人意之处，多多包涵。<br />