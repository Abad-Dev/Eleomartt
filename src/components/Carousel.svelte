<script>
    let animForward  = ['mv0to5', 'mv1to0', 'mv2to1', 'mv3to2', 'mv4to3', 'mv5to4'];
    let animBackward = ['mv0to1', 'mv1to2', 'mv2to3', 'mv3to4', 'mv4to5', 'mv5to0'];
    let class0 = animForward[0];
    let class1 = animForward[1];
    let class2 = animForward[2];
    let class3 = animForward[3];
    let class4 = animForward[4];
    let class5 = animForward[5];

    let classList = [class0, class1, class2, class3, class4, class5];
    
    let currentImage = 3;

    function reset() {
        // Remove animations
        /*img.forEach((image) => {
            animForward.forEach((animation) => {
                image.classL = animForward[L]ist.remove( animation );            
            })
            animBackward.forEach((animation) => {
                image.classList.remove( animation );            
            })
        })
        currentImage=2;*/
    }


    function next(){

    }

    function advance(){
        next();
    }
    function prev(){
    //    previous();		
    }
</script>


<div class="container-fluid">
    <div class="carousel-container">
        <div id="carousel">
            <img src="https://lucidar.me/fr/web-dev/files/img0.svg" id="carousel-image-0" class={"carousel-image " + class0}>
            <img src="https://lucidar.me/fr/web-dev/files/img1.svg" id="carousel-image-1" class={"carousel-image " + class1}>
            <img src="https://lucidar.me/fr/web-dev/files/img2.svg" id="carousel-image-2" class={"carousel-image " + class2}>
            <img src="https://lucidar.me/fr/web-dev/files/img3.svg" id="carousel-image-3" class={"carousel-image " + class3}>
            <img src="https://lucidar.me/fr/web-dev/files/img4.svg" id="carousel-image-4" class={"carousel-image " + class4}>
            <img src="https://lucidar.me/fr/web-dev/files/img5.svg" id="carousel-image-5" class={"carousel-image " + class5}>
        </div>
    
    </div>
    
    <div class="row">
        <div class="col-6 text-end">
            <button class="btn btn-primary" on:click={prev}>Prev</button>
        </div>
        <div class="col-6">
            <button class="btn btn-danger" on:click={advance}>
                Next
            </button>
        </div>
    </div>
</div>

<style>
    .carousel-container{
        height: 300px;
        position: relative;
    }
    #carousel {
    width: 100%;
    max-width: 100vw;
    height: 21vh;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    overflow: hidden;
}

.carousel-image {
    height: 20vh;
    max-height: 200px;
    position: absolute;
    left: 50%;
    border-radius: 7%;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

}

#carousel-image-0 {
    transform: translateX(-50%) translateX(-120%) scale(0.6);
    filter: brightness(40%);
    z-index: 1;
}

#carousel-image-1 {
    transform: translateX(-50%) translateX(-80%) scale(0.8);
    filter: brightness(65%);
    opacity: 1;
    z-index: 2;
}

#carousel-image-2 {
    transform: translateX(-50%) scale(1);
    filter: brightness(100%);
    opacity: 1;
    z-index: 3;
}

#carousel-image-3 {
    transform: translateX(-50%) translateX(80%) scale(0.8);
    filter: brightness(65%);
    opacity: 1;
    z-index: 2;
}

#carousel-image-4 {
    transform: translateX(-50%) translateX(120%) scale(0.6);
    filter: brightness(40%);
    opacity: 1;
    z-index: 1;
}

#carousel-image-5 {
    transform: translateX(-50%) scale(1.5);
    filter: brightness(40%);
    opacity: 0;
    z-index: 1;
}

/* Forward */
.mv0to5 {
    animation: 0.3s ease-out mv0to5;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv5to4 {
    animation: 0.3s ease-out mv5to4;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv4to3 {
    animation: 0.3s ease-out mv4to3;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv3to2 {
    animation: 0.3s ease-out mv3to2;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv2to1 {
    animation: 0.3s ease-out mv2to1;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv1to0 {
    animation: 0.3s ease-out mv1to0;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

/* Backward */
.mv0to1 {
    animation: 0.3s ease-out mv0to1;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv1to2 {
    animation: 0.3s ease-out mv1to2;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv2to3 {
    animation: 0.3s ease-out mv2to3;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv3to4 {
    animation: 0.3s ease-out mv3to4;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv4to5 {
    animation: 0.3s ease-out mv4to5;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

.mv5to0 {
    animation: 0.3s ease-out mv5to0;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

    



@keyframes mv0to5 {
    0% { transform: translateX(-50%) translateX(-120%) scale(0.6); filter: brightness(40%); opacity: 1; z-index: 2}
    20% { opacity: 0; }
    100% { transform: translateX(-50%) scale(0.6);  filter: brightness(40%); opacity: 0; z-index:1}
}
@keyframes mv5to4 {
    0% { transform: translateX(-50%) scale(0.6);  filter: brightness(40%); opacity: 0; z-index:1 }    
    80% { opacity: 0;}
    100% { transform: translateX(-50%) translateX(120%) scale(0.6);  filter: brightness(40%); opacity: 1; z-index: 2 }
}
@keyframes mv4to3 {
    0% { transform: translateX(-50%) translateX(120%) scale(0.6); filter: brightness(40%); opacity: 1; z-index: 2; }
    100% { transform: translateX(-50%) translateX(80%) scale(0.8); filter: brightness(65%); opacity: 1; z-index: 3; }
}
@keyframes mv3to2 {
    0% { transform: translateX(-50%) translateX(80%) scale(0.8); filter: brightness(65%); opacity: 1; z-index: 3; }
    30% { opacity: 1; z-index: 4;}
    100% { transform: translateX(-50%) translateX(0%) scale(1); filter: brightness(100%); opacity: 1; z-index: 4; }
}
@keyframes mv2to1 {
    0% { transform: translateX(-50%) translateX(0%) scale(1); filter: brightness(100%); opacity: 1; z-index: 4; }    
    100% { transform: translateX(-50%) translateX(-80%) scale(0.8); filter: brightness(65%); opacity: 1; z-index: 3; }
}
@keyframes mv1to0 {
    0% { transform: translateX(-50%) translateX(-80%) scale(0.8); filter: brightness(65%); opacity:1; z-index:3; }        
    100% { transform: translateX(-50%) translateX(-120%) scale(0.6); filter: brightness(40%); opacity:1; z-index:2; }
}


@keyframes mv0to1 {    
    0% { transform: translateX(-50%) translateX(-120%) scale(0.6); filter: brightness(40%); opacity:1; z-index:2; }
    100% { transform: translateX(-50%) translateX(-80%) scale(0.8); filter: brightness(65%); opacity:1; z-index:3; }    
}
@keyframes mv1to2 {
    0% { transform: translateX(-50%) translateX(-80%) scale(0.8); filter: brightness(65%); opacity:1; z-index:3; }
    30% { opacity:1; z-index:4;}
    100% { transform: translateX(-50%) translateX(0%) scale(1); filter: brightness(100%); opacity:1; z-index:4; }    
}
@keyframes mv2to3 {    
    0% { transform: translateX(-50%) translateX(0%) scale(1); filter: brightness(100%); opacity:1; z-index:4; }
    100% { transform: translateX(-50%) translateX(80%) scale(0.8); filter: brightness(65%); opacity:1; z-index:3; }
}
@keyframes mv3to4 {    
    0% { transform: translateX(-50%) translateX(80%) scale(0.8); filter: brightness(65%); opacity:1; z-index:3; }
    100% { transform: translateX(-50%) translateX(120%) scale(0.6); filter: brightness(40%); opacity:1; z-index:2; }
}
@keyframes mv4to5 {    
    0% { transform: translateX(-50%) translateX(120%) scale(0.6);  filter: brightness(40%); opacity:1; z-index:2 }
    20% {opacity:0;}
    100% { transform: translateX(-50%) scale(0.6);  filter: brightness(40%); opacity: 0; z-index:1 }
}
@keyframes mv5to0 {
    0% { transform: translateX(-50%) scale(0.6);  filter: brightness(40%); opacity: 0; z-index:1}    
    80% {opacity:0;}
    100% { transform: translateX(-50%) translateX(-120%) scale(0.6);  filter: brightness(40%); opacity: 1; z-index:2}    
}

</style>