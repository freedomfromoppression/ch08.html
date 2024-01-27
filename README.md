# ch08.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>이미지 슬라이드 효과</title>
    <script>
        let files= ["./img/두더지.PNG","imagaes.jpg"];

        let imgs = [];


        let obj;//화면 ing
        let idx=0;//
        for(let i=0; i<files.length; i++){
            imgs[i]= new Image();  //이미지 객체 생성 
            imgs[i].src = files[i]; //이미지 경로 할당(load하도록)
 }
        window.onload=function(){
            obj = document.getElementById('img_id');
            setInterval(fn_right, 1000);
        }
        function fn_left(){
            if(idx == 0){
                idx = imgs.length -1;
            }else{
                idx--;
            }
        obj.src = imgs[idx].src;
        }
        function fn_right(){
            if(idx == imgs.length -1){
                idx = 0;
            }x++else{
                id;
            }
            obj.src = imgs[idx].src;
        }

    </script>
</head>
<body>
    <div>
        <button id="left" type="button" onclick="fn_left()"></button>
        <img src="./images.jpg" id="img_id" alt="">
        <button id ="right" type="button" onclick="fn_right()">></button>
    </div>
    
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>이미지 크기 출력</title>
     <script>
        function fn_change(){
            let sel = document.getElementById("sel");
            let img = document.getElementById("myImg");
            img.onload = function(){
                let mySpan = document.getElementById('mySpan');
                myspan.innterHTML = img.width+ 'x' +img.height;
            }
            let dix = sel.selectedIndex;
            img.src = sel.options[idx].value; 

        }
     </script>

