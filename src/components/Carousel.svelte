<script>
    import Video1 from "../assets/video1.mp4";
    import Video2 from "../assets/video2.mp4";
    import Video3 from "../assets/video3.mp4";
    import Video4 from "../assets/video4.mp4";
    import Video5 from "../assets/video5.mp4";
    import Video6 from "../assets/video6.mp4";

    let animForward  = ['mv0to5', 'mv1to0', 'mv2to1', 'mv3to2', 'mv4to3', 'mv5to4'];
    let animBackward = ['mv0to1', 'mv1to2', 'mv2to3', 'mv3to4', 'mv4to5', 'mv5to0'];

    let classList = JSON.parse(JSON.stringify(animForward));
    
    let currentImage = 3;
    let counterCurrentImage = 3;

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
        
        classList = classList.map((elClassName, index) => {
            return animForward[(counterCurrentImage+2+index)%6]
        })

        if (counterCurrentImage <= 0){
            counterCurrentImage = 5;
        } else{
            counterCurrentImage -= 1;
        }
        if (currentImage >= 5){
            currentImage = 0;
        } else{
            currentImage += 1;
        }
    }

    function previous(){
        classList = classList.map((elClassName, index) => {
            return animBackward[(counterCurrentImage+2+index)%6]
        })

        if (counterCurrentImage >= 5){
            counterCurrentImage = 0;
        } else{
            counterCurrentImage += 1;
        }

        if (currentImage <= 0){
            currentImage = 5;
        } else{
            currentImage -= 1;
        }
    }

    function advance(){
        next();

        console.log(currentImage)
    }
    function prev(){
        previous();		

        console.log(currentImage)
    }
</script>


<div class="container-fluid">
    <div class="carousel-container">
        <div id="carousel">
            <video muted autoplay loop id="carousel-image-0" class={"carousel-image " + classList[0]}>
                <source src={Video1} type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <video muted autoplay loop id="carousel-image-1" class={"carousel-image " + classList[1]}>
                <source src={Video2} type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <video muted autoplay loop  id="carousel-image-2" class={"carousel-image " + classList[2]}>
                <source src={Video3} type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <video muted autoplay loop  id="carousel-image-3" class={"carousel-image " + classList[3]}>
                <source src={Video4} type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <video muted autoplay loop  id="carousel-image-4" class={"carousel-image " + classList[4]}>
                <source src={Video5} type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <video muted autoplay loop  id="carousel-image-5" class={"carousel-image " + classList[5]}>
                <source src={Video6} type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
    
    </div>
    
    <div class="row">
        <div class="col-6 d-flex flex-column align-items-end">
            <button class="btn" on:click={prev}>
                ◀
            </button>
        </div>
        <div class="col-6">
            <button class="btn" on:click={advance}>
                ▶
            </button>
        </div>
    </div>
</div>

<style>
    .btn{
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        background-color: var(--ele-blue);
        border: 1px solid transparent;
        font-size: 30px;
        height: 50px;
        width: 50px;
        color: white;

        transition-duration: .2s;
    }

    .btn:hover{
        background-color: var(--ele-red);
        color: white;
    }
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