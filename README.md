# mouse
鼠标事件
```
<script>
        var hit=document.getElementById('mouseHit');
        hit.addEventListener('mousedown',mouseDownHandle);//鼠标按下事件
        hit.addEventListener('mousemove',mouseMoveHandle);//鼠标移动事件
        hit.addEventListener('mouseup',cancelMoveHandle);//鼠标抬起事件
        hit.addEventListener('mouseout',cancelMoveHandle);//鼠标移开事件
        var isMouseDown = false;//标识鼠标当前是否处于按下状态
         var startX = 0;//定义开始移动的x轴位置
         var startY = 0;
        function mouseDownHandle(event){
                isMouseDown = true;
                startX = event.pageX - hit.offsetLeft;
pageX属性用于返回鼠标指针相对于当前文档左边缘的位置

                startY = event.pageY - hit.offsetTop;
      }
        function mouseMoveHandle(event){
                if(isMouseDown){
                 hit.style.left = event.pageX - startX + 'px';
                 hit.style.top = event.pageY - startY + 'px';
                   }
      }
        function cancelMoveHandle(event){
                isMouseDown = false;
              }
    </script>
```



