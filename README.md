# CONFETTI SHOW
This is my very first web page and also my first experience with html, css and js. I wanted to create an interactive and animated web page because of my Fx TD background, so I decided to build my website with **confetti animation** and **animated buttons**. My main purpose in this project is these two things.

## Beginning

I created my html file. And I put `<!DOCTYPE html>` to make a web page. I put `<head> </head>` for metadata. I created my body part with `<body> </body>`.

To change my tab name, I put `<title> confetti show </title>`.

I created my heads, titles, background image, canvas and scripts in `<body>`.

## HTML

**I created my canvas for java animation and put my thirt party confetti doc.**
    
```    
    <canvas id="my-canvas"></canvas>
    <script src="index.min.js"></script>
```

**I created two buttons, one to start the animation and other to end it, then centred all things with `<center>`.**
```
 <div>
    <h1>Welcome to Confetti Party!</h1>
     <p>Hello user, this website created to celebrate you.</p>
     <h2>PLEASE ENJOY!</h2>
     
     <div>
     <button id="confetti" class="pill">CONFETTI TRIGGER</button>
     <button id="confetti" class="pill_1">FINISH IT</button>
```



**I built my script with `<script>` to put java scripts and to give start and finish animation functions to buttons.**
```
  <script>
   
            let pill= document.querySelector('.pill');
            let confe = document.querySelector('#my-canvas');
            let pill_1 = document.querySelector('.pill_1')
            
            var confettiSettings = { target: 'my-canvas' };
            var confetti = new ConfettiGenerator(confettiSettings);
            confetti.render();
            pill.onclick = function(){
                confe.classList.add('active');
             
            }
            pill_1.onclick = function(){
                confe.classList.remove('active');
                
            }
            </script>
    <p1>This website created by Erem Ryan TEZCAN</p1>
 ```

## CSS
    
 **I used a box for background image. I adjusted the image size and used `background-size: cover;` to avoid repetition of the picture.**
   ``` 
   .box{
background-image: url(../test_erem_ryan/background.jpg);
width: 100%;
height: 100%;
top: 0;
left: 0;
position:absolute;
background-size: cover;
z-index: -2;
}
```
**I adjusted my texts, such as colour, potion, etc...**
```
h1{
    color: rgb(37, 90, 134);
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-size: 50px;
  
    

}
P{

    color: rgb(0, 117, 53);
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bolder;
    font-size: large;
    
    
}
h2{

    color: black;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bolder;
    font-size: large;
    white-space: nowrap;
    position: fixed;
    transform: translate(750%, 50%);

}
p1{
    position: fixed;
    bottom: 0px ;
    left: 15px;
    margin: 20px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
    color: rgb(0, 0, 0);

}
```

**I personalised my button without animation.**
```
.pill
{
    box-shadow: 0px 8px 2px 0px #11496e;
   border: 3px solid #ffffff;
   background: transparent;
    padding: 25px 25px;
    font-size: 20px;
    font-family: fantasy;
    cursor: pointer;
    position: absolute;
    color: #fff;
    text-transform: uppercase;
    transform: translate(-50%, +500%);
    overflow: hidden;
    cursor: pointer;
    transition: .25s;
```
**I created "before click button design". I used content and give background to create my animation layer and I adjusted its position, radius and gave a rotation animation. I used `overflow:hidden` on above to hide my animation layers that is out of button part**
```
.pill::before{
    content: "";
    height: 350px;
    width: 350px;
    background: rgb(5, 197, 255);
    position:absolute;
    left:60%;
    top: 25%;
    transform: translate(-50%);
    z-index: -2;
    border-radius: 150px;
    animation: wave 5s infinite linear;
    transform: translate(-50%) rotate(150deg);
    transition: 2s;
}
```
**I used `hover` to make a rising wave animation, when the cursor comes over to the button.**
```
.pill:hover::before{

        top: -15%;

}
```

**I duplicated these codes for creating a second wave layer in the animation. I changed 'before' expression to 'after' to avoid clashing two layers animation, then I adjusted my second layer animation position and height.**
```
.pill::after{
    
    content: "";
    height: 350px;
    width: 350px;
    background: rgb(54, 173, 241);
    position:absolute;
    left:60%;
    top: 28%;
    transform: translate(-50%);
    z-index: -1;
    border-radius: 150px;
    animation: wave 5s infinite linear;
    transform: translate(-50%) rotate(200deg);
    transition: 2s;
}
@keyframes wave{
    0%{
        transform: translate(-50%)rotate(-180deg);
    }
  
}
.pill:hover::after{

        top: -10%;

}
```
**I designed after click button**
```
.pill:active{

    color: #786fd3;
    border: 3px solid #786fd3;
    box-shadow: 0px 10px 0px 1px #786fd3;

}
```
**I did it same thing for second button.** 


**I adjusted my canvas size and position for confetti effect. I hid my canvas until switch active. I gave a opacity animation.**
```
#my-canvas{

        position: absolute;
        background: transparent;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
    visibility: hidden;
}
#my-canvas.active{
    animation: fade 2s linear ; 
    visibility: visible;
    transition: .10s;
}
@keyframes fade
{
    0%{
        opacity: 0%;
    }
}

```

# THANK YOU,
### EREM RYAN TEZCAN.
