# swift
---------Write a swift program to accept two integer value and return true if one of them is 20. 

func check(a: Int, b: Int) -> Bool {
    if a == 20 || b == 20 {
        return true
    } else {
        return false
    }
}

let a = 21
let b = 22
if check(a: a, b: b) {
    print("One of them number is 20")
} else {
    print("None of them number is not 20")
}

--------Write a Swift program that accept two integer values and to test which value is 
nearest to the value 10, or return 0 if both integers have same distance from 10.

func nearestTo10(a: Int, b: Int) -> Int {
  let distanceA = abs(a - 10)
  let distanceB = abs(b - 10)
  if distanceA < distanceB {
    return a
  } else if distanceA > distanceB {
    return b
  } else {
    return 0
  }
}

let a = 15
let b = 5
let nearest = nearestTo10(a: a, b: b)
print(nearest)

-------Write a Swift program to check if a given non-negative number is a multiple of 3 or a multiple of 5.

func isMultipleOf3Or5(number: Int) -> Bool {
  return number % 3 == 0 || number % 5 == 0
}

let number = 15
let isMultiple = isMultipleOf3Or5(number: number)
print(isMultiple)


--------------Write a Swift program to compute the sum of the two integers. If the values are equal return triple their sum.

func sumOfIntegers(a: Int, b: Int) -> Int {
  if a == b {
    return 3 * (a + b)
  } else {
    return a + b
  }
}

let a = 10
let b = 10
let sum = sumOfIntegers(a: a, b: b)
print(sum)


---------Write a Swift program to add "Is" to the front of a given string. However, if the string already begins with "Is", return the given string.

func addIs(string: String) -> String {
  if string.hasPrefix("Is") {
    return string
  } else {
    return "Is" + string
  }
}

let string = "Hello"
let newString = addIs(string: string)
print(newString) // "IsHello"

let string2 = "IsGood"
let newString2 = addIs(string: string2)
print(newString2)

------Write a Swift program to find the largest number among three given integers.

import Foundation
func findLargestNumber(numbers: [Int]) -> Int {
  var largestNumber = numbers[0]
  for number in numbers {
    if number > largestNumber {
      largestNumber = number
    }
  }
  return largestNumber
}

let numbers = [60, 20, 30]
let largestNumber = findLargestNumber(numbers: numbers)
print("The largest number is \(largestNumber)")


------Write a Swift program to test whether the last digit of the two given non-negative integer values are the same or not.
May 29, 2023
 func lastDigitIsSame(x: Int, y: Int) -> Bool {
  let xLastDigit = x % 10
  let yLastDigit = y % 10
  return xLastDigit == yLastDigit
}

let x = 10
let y = 51

if lastDigitIsSame(x: x, y: y) {
  print("The last digits are the same.")
} else {
  print("The last digits are not the same.")
}


-------Write a Swift program to accept two integer values and return true if one is negative and one is positive. Return true only if both are negative.
May 28, 2023
 func oppositeSigns(x: Int, y: Int) -> Bool {
  if x < 0 && y > 0 || x > 0 && y < 0 {
    return true
  } else {
    return false
  }
}

let x = -2
let y = 11

if oppositeSigns(x: x, y: y) {
  print("The numbers have opposite signs.")
} else {
  print("The numbers do not have opposite signs.")
}
