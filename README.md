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
