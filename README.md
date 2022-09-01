# Assigment
This is my very first web page and also my first experience with html, css and js. I wanted to create an interactive and animated web page because of my Fx TD background so I decided to build my website with **confetti animation** and **animated buttons**. My main purpose in this project is these two things.

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
