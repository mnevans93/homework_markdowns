# Hackerrank Problem #1
```
function plusMinus(arr) {
    let posTotal = 0, zeroTotal = 0, negTotal = 0
    arr.forEach(element => {
        if (element > 0) {
            posTotal += 1
        } else if (element === 0) {
            zeroTotal += 1
        } else {
            negTotal += 1
        }
    })
    let posRatio = (posTotal / arr.length).toFixed(6)
    let zeroRatio = (zeroTotal / arr.length).toFixed(6)
    let negRatio = (negTotal / arr.length).toFixed(6)
    console.log(posRatio + "\n" + negRatio + "\n" + zeroRatio)
}
```

My approach consisted of running through each element of the array and updating counter variables based on whether the element was positive, negative, or zero. We then need a ratio which can be calculated by dividing the count for each by the length of the array. Once we have the three ratios, we just need to console.log them separated on their own lines which we can do by separating each one with a "\n"