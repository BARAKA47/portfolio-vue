<template>
  <v-container>
          <v-col cols='12' md='6'>
          <p class="poppins text-justify">A software engineer with experience in several programming languages as well as a background in entrepreneurship. Graduated from the Faculty of Engineering, Computer Department. A natural problem solver who is keen on finding efficient and durable solutions. Close to 10 years of coding experience in a personal and professional capacity.</p>
         </v-col>

        <div class="orbit">
  
          <ul class="orbit-wrap">
            
            <li class="orbit-center">
              <i class="orbit-center__icon fa fa-code"></i>
            </li>

            <li>
              <ul class="ring-1">
                <li><v-img src= "src/assets/skills/aws.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/docker.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/graphql.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/linux.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/git.png" class="orbit-icon fa invert"></v-img></li>
              </ul>
            </li>
            <li>
              <ul class="ring-2">
                <li><v-img src= "src/assets/skills/html-5.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/css-3.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/vue.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/flutter.png" class="orbit-icon fa invert"></v-img></li>
              </ul>
            </li>
            <li>
              <ul class="ring-3">
                <li><v-img src= "src/assets/skills/python.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/cpp.png" class="orbit-icon fa invert"></v-img></li>
                <li><v-img src= "src/assets/skills/java.png" class="orbit-icon fa invert"></v-img></li>
              </ul>
            </li>

          </ul>
          
        </div>
        
  </v-container>
</template>

<script setup>

</script>
<style lang = 'scss' scoped>
.title {
  color: white !important;
  font-family: "Kaushan Script", cursive;
  font-size:5rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}
.poppins {
  color: white !important;
  font-family: 'Poppins';
  font-size: 1.2rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}


$orbitItemSize: 2em;
$map: (ring-0: 4, ring-1: 5, ring-2: 4, ring-3: 3);
$lastRing: 3;

.orbit{
transform: translate(30%, 0%);
}

.orbit-icon {
  width: $orbitItemSize;
  height: $orbitItemSize;
  line-height: $orbitItemSize;
  font-size: 1.2em;
  border-radius: 50%;
  text-align: center;
  display: block;
}

.orbit-wrap {
  list-style: none;
  font-size: 1.3em;
  
  > li {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    
    /* &:hover {
      ul {
        border-width: 2px;
        border-color: #fff;
      }
      ~ li ul {
        border-color: rgba(255, 255, 255, 0.2);
        li {
          opacity: 0.4;          
        }
      }
    } */
    
  }
}

ul[class^=ring] {
  @extend %ring;
  transition: all 300ms ease-in-out;
  li {
    @extend %orbiting-object;
    transition: all 300ms ease-in-out;
  }
}

@mixin orbit-item($numItems, $numRing) {
  @for $s from 1 through $numItems {  
    // Spread items over the ring
    $deg: 380deg / $numItems;
    
    .ring-#{$numRing} > *:nth-of-type(#{$s}) {
      transform: rotate($s * $deg) translate(12.5em - ($numRing * 2.5)) rotate(-$s * $deg);
    }
  }
}

// Render rings
@for $i from 0 through $lastRing {  
  .ring-#{$i} {
    // decrease each ring in size
    width: 25em - ($i * 5);
    height: 25em - ($i * 5);
    animation: clockwiseRotate 35s - ($i * 5) linear infinite;
    
    .invert {
      animation: counterClockwiseRotate 35s - ($i * 5) linear infinite;
    }
  }
  
  @include orbit-item(map-get($map, ring-#{$i}), $i);
}


%ring {
  border: solid 1px rgba(33, 150, 243, 0.8);
  position: relative;
  padding: 0;
  border-radius: 50%;
  list-style: none;
  box-sizing: content-box;
}

%orbiting-object {
  display: block;
  position: absolute;
  top: 50%;
  left: 50%;
  width: $orbitItemSize;
  height: $orbitItemSize;
  margin: -$orbitItemSize / 2;
}

/*
  center;
*/
.orbit-center {
  z-index: 5;
  font-size: 2em;
  width: 1.8em;
  height: 1.8em;
  line-height: 1.8em;
  text-align: center;
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  
  /* &:hover .orbit-center__icon {
    transform: rotateZ(0deg);
  } */
}
.orbit-center__icon {
  transform: rotateZ(-360deg);
  transition: all 300ms ease-in-out;
}
/* .orbit-wrap > li.orbit-center:hover ~ li > ul {
  width: 0;
  height: 0;
  * {
    transform: translate(0, 0);
  }
} */

/* 
animations 
*/
@keyframes clockwiseRotate {
    from {
        transform: rotate(0deg)
    }
    to {
        transform: rotate(360deg)
    }
}

@keyframes counterClockwiseRotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
      transform: rotate(-360deg);
  }
}




</style>


