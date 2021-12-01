<template>
  <div>
    <h1>{{ msg }}</h1>
    <div class="container">
        <div class="content">
            <img class="sam" src="/sam4.svg">
            <img class="sam_braco" src="/sam_braco.svg">
            <div class="eye">
                <div class="eye-1"></div>
                <div class="eye-2"></div>
            </div>
            <div class="mouth1">
                <div class="mouth-one1"></div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Assistente',
  props: {
    msg: String
  }
}
</script>

<style>

.container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.content {
    width: 600px;
    height: 600px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgb(112, 189, 147);
    opacity: 1;
    border-radius: 20px;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
}

.eye {
    position: absolute;
    width: 200px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    top: 27%;
    left: 44%;
    border-radius: 20px 20px 20px 20px;
    background-color: #003;
    z-index: 1050;
}

.eye-1 {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #2fa1dc;
    animation: eye 4s ease-out infinite;
}

.eye-2 {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #2fa1dc;
    animation: eye 4s ease-out infinite;
}

@keyframes eye {
    0% {
        height: 0;
    }

    10% {
        height: 50px;
    }

    20% {
        height: 0;
    }

    30% {
        height: 50px;
    }

    100% {
        height: 50px;
    }
}

.mouth {
    position: absolute;
    width: 250px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    top: 35%;
    left: 42.7%;
}

.sam {
    z-index: 1050;
}

.mouth-one {
    width: 90px;
    height: 40px;
    position: relative;
    border-radius: 0 0 50% 50%;
    background-color: #fff;
}

@keyframes sam-auto {
    to {
        transform: translateY(-10px);
    }

    from {
        transform: translateY(0);
    }
}

.sam_braco {
    position: absolute;
    left: 50.2%;
    top: 46%;
    animation: braco_sam 4s ease-in-out alternate infinite;
}

@keyframes braco_sam {
    0% {
        transform: rotateZ(-45deg);
        transform-origin: 20% 40%;
    }

    10% {
        transform: rotateZ(10deg);
    }

    20% {
        transform: rotateZ(-45deg);
        transform-origin: 20% 40%;
    }

    30% {
        transform: rotateZ(10deg);
    }

    100% {
        transform: rotateZ(0deg);
    }
}

@media only screen and (max-width: 600px) {

   h1 {
       margin-top: 100px;
   }

    .content {
        width: 400px;
        height: 400px;
    }

    .eye {
        width: 150px;
        height: 60px;
        top: 32%;
        left: 30%;
    }

    .eye-1 {
        width: 30px;
        height: 30px;
    }

    .eye-2 {
        width: 30px;
        height: 30px;
    }

    .sam_braco {
        top: 50%;
        width: 140px;
    }

    img {
        width: 300px;
    }
}
</style>
