# 20. How to Use Anticipation in Animation

### rotation bounce expression after effects

```jsx
amp = 0.5;
freq = 1.5;
decay = 2.0;
n = 0;
time_max = 4;
if (numKeys > 0) {
  n = nearestKey(time).index;
  if (key(n).time > time) {
    n--;
  }
}
if (n == 0) {
  t = 0;
} else {
  t = time - key(n).time;
}
if (n > 0 && t < time_max) {
  v = velocityAtTime(key(n).time - thisComp.frameDuration / 10);
  value + (v * amp * Math.sin(freq * t * 2 * Math.PI)) / Math.exp(decay * t);
} else {
  value;
}
```

### output

![](<./01%20-%20Cup%20(To%20Begin)_2.gif>)
