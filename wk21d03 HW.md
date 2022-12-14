# Hackerrank Problem #3
```
function timeConversion(s) {
    let hr = parseInt(s.slice(0, 2))
    let min = s.slice(3, 5)
    let sec = s.slice(6, 8)
    let timeOfDay = s.slice(8, 10)
    
    if (timeOfDay === "AM") {
        if (hr === 12) {
            hr = "00"
        } else {
            hr = `${hr}`
            if (hr.length === 1) {
                hr = `0${hr}`
            }
        }
    } else {
        if (hr === 12) {
            hr = "12"
        } else {
            hr = `${12 + hr}`
        }
        
    }
    
    return `${hr}:${min}:${sec}`
}
```
For this problem, I looked to slice the initial string into parts. The hour portion is the most complicated; the minute and second values translate directly to the output string without any further manipulation.

To generate the hour portion, we need to check whether it is AM or PM because that will offset the hour value by either 0 or 12 hours. If it is AM and it is 12 AM exactly, that is 00; otherwise, the output "hr" string will be equivalent to the input except with a prepended 0 if the hour is 1 - 9. If it is PM, it will either be 12 PM exactly or 12 + whatever the input hour value is. Before doing any of these checks, I parsed the "hr" value to an integer so in the event the time is PM, "hr" can be generated by adding 12 to it before re-converting back to a string.