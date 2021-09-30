## 3D Cube with animations... Only CSS👀 feat.Nar


<iframe height="350" style="width: 100%;" scrolling="no" title="CSS Cube [Naruto]" src="https://codepen.io/reboot13/embed/wvdWQGb?default-tab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/reboot13/pen/wvdWQGb">
  CSS Cube [Naruto]</a> by Krutik Raut (<a href="https://codepen.io/reboot13">@reboot13</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Let's Get Started 

Apart from basic CSS properties, I have used some properties which change the 2D page of the view to a 3D one.

**CSS properties:**
1. perspective

2. perspective-origin

3. transform-style

4. transform (translate/rotate)


To make a 3D cube we have to first make a block that contains the structure of the cube


Lets White HTML first


```
<div class="scene">
  <div class="box">
    <div class="top"></div>
    <div class="bottom"></div>
    <div class="left"></div>
    <div class="right"></div>
    <div class="back"></div>
    <div class="front"></div>
  </div>
</div>
``` 


The scene contains the body of the cube, I have given the CSS class names to the sides of the cube which I guess makes sense to you all.


**Adding the Magic of CSS**


```
body {
  background-color: #ff9152;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  perspective: 20em;
  perspective-origin: 50% calc(50% - 10em);
}

``` 


1. I have given a background color to the body, used flex to center the elements 
Use the perspective property to make the body 3D

Checkout docs for perspective at W3school:  [click here](https://www.w3schools.com/cssref/css3_pr_perspective.asp) 

2. Setting *perspective-origin* by calculating the height of the body

The perspective-origin property defines at which position the user is looking at the 3D-positioned element.



```
.scene {
  position: relative;
  transform-style: preserve-3d;
  animation: rotateX 7s infinite linear;
}
``` 

Setting the position  to relative so the elements inside it can be positioned to absolute
respective to the scene

Adding a *transform-style: preserve-3d*  

The transform-style property specifies how nested elements are rendered in 3D space.


Now let us style the cube:


```
.box {
  height: 120px;
  width: 120px;
  position: relative;
  transform-style: preserve-3d;
  animation: rotateY 5s infinite linear;
}
``` 

Just gave some height, position, and animation

**Styling the sides of the Cube**


```
.top,
.bottom,
.left,
.right,
.front,
.back {
  position: absolute;
  height: 120px;
  transform-style: preserve-3d;
  width: 120px;
  background-color: rgba(20, 116, 241, 0.281);
background-size:cover; 
box-sizing:border-box;
border: 5px solid #fff;
}
.front {
  transform: translateZ(3.7rem);
  background-image: url("https://cdn140.picsart.com/355182439052201.jpg?to=crop&type=webp&r=310x310&q=75");
background-size:cover;
}

.right {
  transform: rotateY(270deg) translateZ(3.7rem);
background-image: url("http://pm1.narvii.com/7533/be35ca4f98dd1790e03d932bc70c8d3588359105r1-281-281v2_uhq.jpg")

}
.back {
  transform: rotateY(180deg) translateZ(3.7rem);
background-image:url("https://cdn.costumewall.com/wp-content/uploads/2018/09/sasuke-uchiha.jpg");
background-size:cover;
}
.left {
  transform: rotateY(90deg) translateZ(3.7rem);
background-image:url("https://i1.sndcdn.com/avatars-000736438537-zvc9fi-t240x240.jpg");
background-size:cover;
}

.top {
  transform: translateY(-50%) rotateX(90deg);
scaleY(-1);
background-image:url("https://i.pinimg.com/originals/c2/c6/87/c2c687c78da549431b8903e0aad90184.png");
background-size:cover;
}
.bottom {
  bottom: -120px;
  transform: translateY(-50%) rotateX(90deg) scaleY(-1);
background-image: url("https://static.wikia.nocookie.net/08b81b8e-00c6-4f69-83c6-94bfc79f05c7/scale-to-width/755");
background-size:cover;

}
``` 

Using the transform property and with use of translate and rotate will give the desired shape of the cube

Set the background with characters from **#Naruto**


Added Some keyframes to animate the cube

```
@keyframes rotateX{
  25% {
   transform: rotateX(-180deg);
  }
  50% {
    transform: rotateY(-360deg);
 }
  70%{
   transfrom: rotateX(-180deg)
}

  
}

``` 


**And we are done**
















 