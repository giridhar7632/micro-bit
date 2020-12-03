---
name: 'micro:bit Flappy Bird'
description: 'Create a basic Flappy Bird Game using BBC micro:bit'
author: '@giridhar7632'
img: ''
---

Have you ever heard about the popular BBC micro:bit? In this workshop we are going to work with BBC micro:bit and create a basis **Flappy Bird Game** using it. Check out the final project.

![Final Project]()

Here's the [demo/code](https://makecode.microbit.org/_i6g2xLFeTTfP).

## How to play...

The objective is to direct a flying bird :bird:, which is moving continuously to the right, between sets of obstacles. If the player touches an obstacle, they lose. You can check original Flappy Bird Game [here](https://flappybird.io/).

## Prerequisites

Extremely basic knowledge of any programming language. We are going to use JavaScript to code our micro:bit.

If you don't have the hardware, don't worry we'll use stimulator in this workshop. [Makecode's](https://makecode.microbit.org) micro:bit simulator was excellent!

## Getting Started

Micro bit is a tiny piece of hardware with many features. It a pocket size computer which performs what you say. We have to write a computer program and upload it to micro:bit what to do. A micro USB cable is used to transfer the code from PC to micro:bit.

![micro:bit]()

A micro:bit can only do what you tell it to do. You can use different programming languages to write program like [Makecode](https://makecode.microbit.org/), which you can use to code in code blocks or JavaScript. You can also use [Python](https://python.microbit.org/v/2) to program a micro:bit.

On front face, it has 25 LEDs which we will use to display our game.

These are the main parts of a micro:bit:point_down:

![micro:bit parts]()

Learn more about micro:bit [here](https://microbit.org/get-started/user-guide/overview/).

## Setup

Open [Makecode](https://makecode.microbit.org/) and click on :heavy_plus_sign:`New Project`.

![Setup]()

You should see something like this. 

![Project created]()

Once you finish setting up, let's get going:rocket:

## JavaScript

By default MakeCode open's a project with code blocks. At top of the window, switch to JavaScript.

![JavaScript]()

The MakeCode programming environment uses JavaScript along with the Static [TypeScript](https://www.typescriptlang.org/) language. Don't worry about TypeScript. It is super similar to JavaScript. We will use most of the micro:bit’s built-in JavaScript functions.

## Step-1

Let's start with adding the bird. We just have 25 LEDs. Don't expect more. We have to assume a blinking LED as a bird😂

Create a new LED sprite pointing to the right. A sprite is like a little LED creature you can tell what to do.

```js
let bird: game.LedSprite = null
bird = game.createSprite(0, 2)
bird.set(LedSpriteProperty.Blink, 300)
```

A variable `bird` is declared in TypeScript. The syntax of declaring a varible in TypeScript is: `let identifier:data-type = value;`

The `game.createSprite(x,y)` creates a sprite(our bird) in position (x, y) on the 5x5 grid of LEDs. Then we set our bird to blink every 300 milli seconds.

You can see our bird flying like this:point_down:

![blinking LED]()
