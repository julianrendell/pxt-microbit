# Is Gesture

Tests if a gesture is currently detected.

```sig
input.isGesture(Gesture.Shake)
```

## Parameters

* ``gesture`` means the way you hold or move the @boardname@. This can be `shake`, `logo up`, `logo down`, `screen up`, `screen down`, `tilt left`, `tilt right`, `free fall`, `3g`, or `6g`.

## Example: random number

This program shows a number from `2` to `9` when you shake the @boardname@.

```blocks
let dummy = input.acceleration(Dimension.X);
forever(function() {
    if (input.isGesture(Gesture.Shake)) {
        let x = Math.randomRange(2, 9)
        basic.showNumber(x)
    }
})
```

## Note
Unlike [on gesture](/reference/input/on-gesture) there has to be an explicit call to read a value from the accelerometer to initiate gesture detection. It can be a single read in the setup block.

## See Also

[on gesture](/reference/input/on-gesture)
