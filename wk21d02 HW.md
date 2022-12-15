# Hackerrank Problem #2
```
function miniMaxSum(arr) {
    const modArr1 = [...arr]
    const modArr2 = [...arr]
    let min = 0
    let max = 0
    while (modArr1.length > 1) {
        min += Math.min(...modArr1)
        modArr1.splice(modArr1.indexOf(Math.min(...modArr1)), 1)
    }
    while (modArr2.length > 1) {
        max += Math.max(...modArr2)
        modArr2.splice(modArr2.indexOf(Math.max(...modArr2)), 1)
    }
    console.log(`${min} ${max}`)
}
```
For this problem, I set up two arrays that were copies of the input array created using the spread operator. I used Math.min and Math.max to determine the min or max value within these arrays respectively, but then I needed to remove that element from the array using splice so the next iteration of the while loop would then go for second highest/lowest, third, and finally fourth. Splice mutates the target array which is why I set up two copies of the input array for the purposes of this function rather than mutate the input array.