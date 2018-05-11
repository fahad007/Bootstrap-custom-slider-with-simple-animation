## Bootstrap Custom Slider With Simple Animation

This is a bootstrap slider. a few custome has been made. no plugin needed just use Bootstrap4.

### Add this html

```markdown
<section class="main-area">
            <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
                <ol class="carousel-indicators">
                    <li data-target="#carouselExampleControls" data-slide-to="0" class="active">1</li>
                    <li data-target="#carouselExampleControls" data-slide-to="1">2</li>
                    <li data-target="#carouselExampleControls" data-slide-to="2">3</li>
                </ol>

                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <!-- carousel-image -->
                        <div class="moving-area">
                            <div class="moving-div" style="background: url(http://www.bikesrepublic.com/wp-content/uploads/2016/11/2017-KTM-1290-Super-Duke-R-action-03.jpg) no-repeat bottom center / cover;"></div>
                            <!-- carousel-text -->
                            <div class="carousel-text">
                                <div class="container">
                                    <h1>This is slid one</h1>
                                </div>
                            </div>
                        </div>
                        
                    </div>

                    <div class="carousel-item">
                        <!-- carousel-image -->
                        <div class="moving-area">
                            <div class="moving-div" style="background: url(https://i1.wp.com/www.iamabiker.com/wp-content/uploads/2017/01/Ducati-Scrambler-HD-wallpapers-1.jpg) no-repeat center center / cover;"></div>
                            <!-- carousel-text -->
                            <div class="carousel-text">
                                <div class="container">
                                    <h1>This is slid two</h1>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="carousel-item">
                        <!-- carousel-image -->
                        <div class="moving-area">
                            <div class="moving-div" style="background: url(http://www.srpskafabrikastakla.com/image/2018/03/19/2018-ktm-1290-super-duke-r-ktm-1290-super-duke-r-gets-an-update-for-2017_bb1319796f194f01.jpg) no-repeat top center / cover;"></div>
                            <!-- carousel-text -->
                            <div class="carousel-text">
                                <div class="container">
                                    <h1>This is slid three</h1>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
```



### Add this css

```markdown
@import url('https://fonts.googleapis.com/css?family=Teko:400,700');
.main-area{
    width: 100vw;
    height: 100vh;
    position: relative;
    font-family: 'Teko', sans-serif;
}
.moving-area{
    width: 100vw;
    height: 100vh;
    overflow:hidden;
    position: relative;
}
.moving-div{
    position: absolute;
    width: 120%;
    height: 140%;
    top: -20%;
    left: -10%;
    -webkit-filter:blur(2px);
}
.carousel-text {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: right;
}
.carousel-text h1 {
    font-size: 8vw;
    text-transform: uppercase;
    font-weight: 900;
    color: #fff;
    line-height: 1;
    transition: all .4s;
    transform: translateX(-25%);
    text-shadow: 0 0 5px rgba(0,0,0,.2);
}
.carousel-item.active .carousel-text h1 {
    transform: translateX(0);
}
.carousel-indicators {
    position: absolute;
    right: unset;
    bottom: unset;
    left: 0;
    z-index: 15;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    padding-left: 0;
    margin-right: 0;
    margin-left: 0;
    list-style: none;
    top: 0;
    width: 100px;
    height: 100vh;
    background: none;
    flex-flow: column;
    justify-content: center;
    align-items: center;
}
.carousel-indicators li {
    position: relative;
    -webkit-box-flex: 0;
    -ms-flex: 0 1 auto;
    flex: 0 1 auto;
    width: auto;
    height: auto;
    margin-right: 0;
    margin-left: 0;
    text-indent: 0;
    background: none !important;
    font-size: 50px;
    color: #fff;
    z-index: 111111111;
    font-weight: 900;
}
.carousel-indicators .active {
    background-color: none;
}
```

### Add this javascript

```markdown
var windowWidth = $(window).width();
var windowHeight = $(window).height();
$('.moving-area').mousemove(function(event) {
    var moveX = (($(window).width() / 2) - event.pageX) * 0.1;
    var moveY = (($(window).height() / 2) - event.pageY) * 0.1;
    $('.moving-div').css('margin-left', moveX + 'px');
    $('.moving-div').css('margin-top', moveY + 'px');
});
```

### Here is the live link of this project you can check it out
[click here to view the project ](https://fahad007.github.io/Bootstrap-custom-slider-with-simple-animation/). 


