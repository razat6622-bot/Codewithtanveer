<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday ❤️</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    height:100vh;
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff4d6d,#1a001f);
    color:white;
    text-align:center;
}

/* glowing background */
body::before{
    content:"";
    position:absolute;
    width:400px;
    height:400px;
    background:pink;
    filter:blur(140px);
    opacity:0.4;
    animation:glow 5s infinite;
}

@keyframes glow{
    0%{transform:scale(1);}
    50%{transform:scale(1.3);}
    100%{transform:scale(1);}
}

.container{
    position:relative;
    z-index:2;
    padding:20px;
}

/* anime image */
img{
    width:240px;
    border-radius:20px;
    box-shadow:0 0 25px pink;
    margin-bottom:20px;
}

h1{
    font-size:38px;
    margin-bottom:10px;
    color:#fff;
}

p{
    font-size:18px;
    color:#f5d7e3;
    margin-bottom:25px;
}

button{
    padding:14px 24px;
    border:none;
    border-radius:12px;
    background:white;
    color:#ff4d6d;
    font-size:18px;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.1);
}

#message{
    margin-top:25px;
    font-size:23px;
    display:none;
    color:white;
    animation:fade 2s;
    line-height:1.6;
}

@keyframes fade{
    from{opacity:0;}
    to{opacity:1;}
}

/* floating hearts */
.heart{
    position:absolute;
    color:white;
    animation:float 5s linear infinite;
}

@keyframes float{
    0%{
        transform:translateY(100vh);
        opacity:1;
    }
    100%{
        transform:translateY(-10vh);
        opacity:0;
    }
}

</style>
</head>

<body>

<div class="container">

<img src="https://i.imgur.com/QZ6X9Qm.png">

<h1>Happy Birthday ❤️</h1>

<p>For the cutest anime girl ✨</p>

<button onclick="showWish()">Open Your Surprise 🎁</button>

<div id="message">
Happy Birthday to someone really special ❤️<br><br>

Your smile honestly feels brighter<br>
than any anime scene ✨<br><br>

I hope your day becomes as beautiful<br>
as you are 😳💖<br><br>

And maybe...<br>
I like you a little more than I should 😅👉👈
</div>

</div>

<script>

function showWish(){

document.getElementById("message").style.display="block";

/* floating hearts */
setInterval(() => {

let heart=document.createElement("div");

heart.innerHTML="❤️";

heart.className="heart";

heart.style.left=Math.random()*100+"vw";

heart.style.fontSize=(Math.random()*20+15)+"px";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},5000);

},300);

}

</script>

</body>
</html># Codewithtanveer
