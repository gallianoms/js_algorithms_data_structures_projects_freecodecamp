function convertToRoman(num) {
  let result = ''

  const roman = {
    M: 1000,
    CM: 900,
    D: 500,
    CD: 400,
    C: 100,
    XC: 90,
    L: 50,
    XL: 40,
    X: 10,
    IX: 9,
    V: 5,
    IV: 4,
    I: 1,
  }

  for (let key in roman) {
    result += key.repeat(Math.floor(num / roman[key]))
    num %= roman[key]
  }

  return result
}

console.log(convertToRoman(36)) // XXXVI
console.log(convertToRoman(50)) // L
