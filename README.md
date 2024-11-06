# What is GSAP?

- GSAP (GreenSock Animation Platform) is a JavaScript library for animations.
- Used to create smooth, high-performance animations on web pages.

## Core Concepts

1. gsap.to()

- Moves properties from their current value to a specified value.
- Syntax: `gsap.to(target, {duration, properties})`
- Example:
``` javascript

gsap.to(".box", {duration: 1, x: 100});
```

2. **gsap.from()**

- Starts properties from specified values and animates them to their original values.
- Syntax:` gsap.from(target, {duration, properties})`
- Example:

```
gsap.from(".box", {duration: 1, opacity: 0});
```

3. **gsap.fromTo()**

- Defines both starting and ending values for properties.
- Syntax: `gsap.fromTo(target, {fromProperties}, {toProperties})`
- Example:

```
gsap.fromTo(".box", {opacity: 0}, {duration: 1, opacity: 1});

```

4. **gsap.set()**

- Instantly sets properties without animating.
- Syntax:` gsap.set(target, {properties})`
- Example:

```
gsap.set(".box", {x: 200});

```


### Basic Properties

- `x, y:` Position values.
- `scale`: Resizes element.
- `rotation`: Rotates element (in degrees).
- `opacity`: Sets transparency (0 is invisible, 1 is fully visible).
- `duration`: Animation time (in seconds).

***

### Ease Functions

- Eases make animations feel more natural.
- Examples: `Power1.easeIn`, `Power2.easeOut`, `Bounce.easeInOut`
- Syntax: `{ease: "easeType"}`

```
gsap.to(".box", {duration: 1, x: 100, ease: "power2.inOut"});

```

***

### Repeat & Yoyo

- `repeat`: Number of times the animation will repeat.
- `yoyo`: Makes animation go back and forth.
- Example:
```
gsap.to(".box", {duration: 1, x: 100, repeat: 2, yoyo: true});
```

***

### Delays

- `delay`: Time before animation starts (in seconds).
- Example:
```
gsap.to(".box", {duration: 1, x: 100, delay: 0.5});
```

***

### Staggering

- Staggers animations for multiple elements in sequence.
- Syntax: `{stagger: amount}`
- Example:
```
gsap.to(".box", {duration: 1, x: 100, stagger: 0.2});
```

***

### Timeline

- A way to chain multiple animations.

- Syntax:
```
let tl = gsap.timeline();

tl.to(".box1", {duration: 1, x: 100})
  .to(".box2", {duration: 1, y: 100});

tl.play() - Plays timeline
tl.pause() - Pauses timeline
tl.reverse() - Reverses timeline
```

***
### ScrollTrigger Plugin

- Adds animation triggers based on scroll position.
- Basic Syntax:
```
gsap.registerPlugin(ScrollTrigger);
gsap.to(".box", {
  scrollTrigger: ".box",
  duration: 1,
  x: 200
});
```
***
### Common Use Cases

1. Fade In:
```
gsap.from(".element", {duration: 1, opacity: 0});
```
2. Slide in from Left:
```
gsap.from(".element", {duration: 1, x: -200});
```
3. Scale Up:
```
gsap.to(".element", {duration: 1, scale: 1.5});
```
### Quick Tips

1. Use `.to` for final position animations.
2. Use `.from` for animating from initial hidden states.
3. `.fromTo` if starting and ending positions both need defining.
4. `repeat` and `yoyo` add looping effects for smoother animations.
