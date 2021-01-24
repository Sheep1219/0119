<template>
<h1>聯絡資訊
  <h2>國立清華大學藝術學院學士班
30014新竹市南大路521號（教學大樓3F）<br>+886-3-5715131 #78802 / ipta@my.nthu.edu.tw
  <div class="container">
    <div id="p5Canvas"></div>
  </div>
  </h2>
</h1>
</template>

<script>
import P5 from 'p5';
export default {
  data() {
    return {
      p5Canvas: null,
    }
  },
  created() {
    const sketch = p5 => {
        let w = 500;
        let h = 400;
        // let w = window.innerWidth;
        // let h = window.innerHeight;
        p5.setup = () => {
            p5.createCanvas(w, h, p5.WEBGL);
        };
        p5.draw = () => {
            p5.background(1);
            let locX = p5.mouseX - w / 3;
            let locY = p5.mouseY - h / 2;
            p5.ambientLight(50);
            p5.directionalLight(255, 0, 0, 0.25, 0.25, 0);
            p5.pointLight(255, 100, 255, locX, locY, 250);
            p5.push();
            p5.translate(-w / 4, 0, 0);
            p5.rotateZ(p5.frameCount * 0.02);
            p5.rotateX(p5.frameCount * 0.1);
            p5.specularMaterial(250);
            p5.box(100, 100, 100);
            p5.pop();
            p5.translate(w / 4, 0, 0);
            p5.ambientMaterial(250);
            p5.sphere(120, 64);
        };
    }
    this.p5Canvas = new P5(sketch, 'p5Canvas');
  },
  
  unmounted () {
    this.p5Canvas = null;
  }
}
</script>

<style>

#p5Canvas {
  width: 100vw;
  position: relative;
  margin-left: 20%;
}
main {
  margin: 0 auto;
  width: 90vw;
  margin-left: 50%;
}

</style>