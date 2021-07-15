//CSS
1.
        .font-box{
            font-family: 'Open Sans', sans-serif;
            font-size: 20px;
        }
        
2.
        #red-box{
            width: 200px;
            height:200px;
            background:red;
            border:1px green solid;
            position:absolute;
            left:50%;
            top:50%;
            transform: translate(-50%, -50%);
        }
        
        <div id="red-box"></div>
        
3.
        html, body {
            width: 100%;
            height: 100%;
            padding: 0px;
            margin:0px;
        }
        #response-box{
            width: 100%;
            height: 100%;
        }
        @media screen and (min-width: 512px){
            #response-box{
                background:green;
            }
        }
        @media screen and (min-width: 720px){
            #response-box{
                background:purple;
            }
        }
        @media screen and (min-width: 1024px){
            #response-box{
                background:blue;
            }
        }
4.
        #bg-box{
            width: 300px;
            height: 300px;
            background-image: url("bg.jpg");
            background-size:100% 100%;
            background-repeat: no-repeat;
        }
5.
        #blue-circle{
            width: 100px;
            height: 100px;
            border-radius:50%;
            background:blue;
            position: relative;
            animation: move-loop 5s infinite;
        }
        @keyframes move-loop {
            0% {left:0px;}
            50% {left:95%;}
            100% {left:0px;}
        }
6.
        #gredient-btn{
            width: 300px;
            height: 100px;
            background-image: linear-gradient(90deg, #f6b144, #e69220);
        }
7.
        #fade-btn{
            width: 300px;
            height: 100px;
            background:red;
            transition: 0.3s;
        }
        #fade-btn:hover{
            background:green;
        }
8.
        #red-btn{
            width: 150px;
            height: 150px;
        }
        #red-btn:hover{
            width: 300px;
            height: 300px;
        }
9.
        #blue-bg>#green-box{
            position: absolute;
            left:0%;
            top:0%;
            margin:10px;
            width: 30%;
            height:30%;
            background:green;
            border: 1px solid;
        }
        #blue-bg>#red-box{
            position: absolute;
            margin:10px;
            width: 30%;
            height:30%;
            background:red;
            border: 1px solid;
            left:50%;
            top:50%;
            transform: translate(-50%, -50%);
        }
        #blue-bg>#blue-box{
            position: absolute;
            margin:10px;
            width: 30%;
            height:30%;
            background:blue;
            border: 1px solid;
            right:0%;
            bottom:0%;
        }
10.
        #parent{
            font-size:20px;
        }
        #parent>#child{
            font-size:18px;
        }

//JAVASCRIPT
1.      document.getElementById("mylist");

2.
        document.getElementById("box").style.backgroundColor = 'red';
        document.getElementById("box").style.opacity = '0.7';
        document.getElementById("box").style.width = '100px';
        document.getElementById("box").style.height = '100px';
        document.getElementById("box").style.border = '1px solid green';
        
3.
        <input type="text" id="inputData">
          <button type="button" onclick="getInput()">Click</button>
        function getInput() {
            var x = document.getElementById("inputData").value;
        }
        
4. checkbox and radio
<input type="checkbox" id="checkboxData" value="Good">
    <label for="checkboxData">Good</label>
    <button type="button" onclick="getCheckbox()">Click</button>
    <input type="radio" id="radioData" value="Bad">
    
        //checkbox
        function getCheckbox() {
            if(document.getElementById("checkboxData").checked){
            var chk = document.getElementById("checkboxData").value;;
            alert(chk);
            }else{
            alert("Not Check Yet");
            }
        }

        //radio
        function getRadio() {
            if(document.getElementById("radioData").checked){
            var rad = document.getElementById("radioData").value;
            alert(rad);
            }else{
            alert("Not Check Yet");
            }
        }
        
5. select
<select name="selectData" id="selectData" onchange="getSelect()">
        <option value="AAA">AAA</option>
        <option value="BBB">BBB</option>
        <option value="CCC">CCC</option>
    </select>
        //select
        function getSelect(){
            var sel = document.getElementById("selectData").value;
            alert(sel);
        }
        
7. I love You
<div id="love-message"></div>

        setTimeout(() => {
            document.getElementById('love-message').innerText = 'I Love You';
        }, 8000);
        
8. i Like You
<div id="like-message"></div>

        setInterval(() => {
            document.getElementById('like-message').innerText += 'I Like You';
        }, 5000);
        
9.
//alert
<button type="button" id="aws-btn" onclick="alertBox()">Alert</button>

        function alertBox() {
            alert("Alert!!!");
        }
10. Reverse
<div id="reverse-mess">I Love Javascript</div>
    <button type="button" onclick="reverse()">Reverse</button>
            function reverse(){
            document.getElementById('reverse-mess').innerHTML = document.getElementById('reverse-mess').innerText.split("").reverse().join("");
        }
        
11. Video
<video width="400" controls id="video1">
        <source src="video1.mp4" type="video/mp4">
    </video>
    <button id="play-btn" type="button" onclick="playVid()">Play</button>
    <button id="pause-btn" type="button" onclick="pauseVid()">Pause</button>
    
            var vid1 = document.getElementById('video1');
        function playVid(){
            vid1.play();
        }
        function pauseVid(){
            vid1.pause();
        }
        
12. GET
        fetch('https://my.private-server.com/users.json')
        .then(response=>response.json())
        .then(data=>console.log(data));
        
13. POST
        fetch('https://my.private-server.com/save',{
            method: 'POST',
            headers:{
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                name:"John",
                lastname="Adam",
                age:"28",
            })
        })
        .then(response=>response.json())
        .then(data=>console.log(data));
        
14. Multiple
        let number = [1,9,9,3,2,1,3,6];
        let result = [];
        for(let i=0;i<number.length;i++){
            result.push(number[i]*(i+1));
        }
        
15. Filter
        let people = ['adam','wanda','john','sean','danny','jean'];
        const fill = people.filter(people=>people.slice(-1)==='n');
        
17. BodyTag
        document.body.innerHTML = `
        <div id="parent" style="border: 1px solid red">
            <div class="child" style="border: 1px solid blue; background-color: green">
                <span id="inner-message">Hi..</span>
            </div>
        </div>`;

