# Quick Start

There are two ways to start playing with `p5.genzine`.

## Easy Way

You can simply just:

- Duplicate this [p5 sketch](https://editor.p5js.org/munusshih/sketches/WyAAMH2gY) to play in ih the p5 editor
- Fork [this sketch](https://openprocessing.org/sketch/1897656) to utilize the forking function in [Open Processing](https://openprocessing.org/) 
- Play with [this example of Processing-themed Stretching](https://openprocessing.org/sketch/1898736) to better understand it works!

## Do It Yourself

First, import the p5.genzine library in by pasting the below line after the `<body></body>` tag

```HTML
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.6.0/p5.js"></script>
<script src="https://munusshih.github.io/p5.genzine/p5.(gen)zine.js"></script>
<script src="sketch.js"></script>
```

And then, create a starter file called `sketch.js` and paste the below code in;
```javascript
const zine = {
  title: "GenZ(ine) V1.2",
  author: "Munus Shih",
  personalUrl: "https://munusshih.com",
  frameCount: 8,
  description: "Our objective is to create a coded zine that focuses on digital identity. We will use P5.js to teach ‘function’ and generate a collaborative digital profile zine in the end. We created some customized functions for people to play with this zine more easily."
}

function drawPage() {

/* Cover */
  cover.randomLayout(["hello world", selfie])

/*page One*/
  one.rect(one.mouseX, one.mouseY, 100)

/*page Two*/
  two.background(random(255), random(255), random(255))
  two.glitchLayout(["hello world", selfie])

/*page Three*/
  three.gridLayout(["hello world", selfie])

/*back Cover*/
  back.background(random(255), random(255), random(255))
}

```

## Your First Function 💖
The library basically does everything that the p5 library does, while simply using `namespacing` to specify where you want to draw your shape.

For instance, if you want to draw a circle on the cover page, you will write.

```javascript
function drawPage(){
  cover.circle(30, 30, 10)
}
```

The `drawPage()` function here basically replace the original p5 `draw()` function.

You can always hit the button to download your zine as a `.jpg` or `.pdf` that's ready to print! You can also share your source code to friends so they can play with your zine and get inspried :)