# Overview

For each sub section below read the prompt, identify the expectations and write the specification that can be used to write tests for that prompt.

# Unit Test

A function called `add` that takes an array of numbers and returns the sum.

## Expectations:

- takes an array of numbers
- returns the sum of the numbers in the array
  - the sum should be a number
- should throw an error if you pass an array of strings instead of numbers
- should work with negative numbers, too
- should return 0 if an empty array is passed through

## Test Specs

Unit test specifications should take the form of: Expect [action] to be [some result]

1. Expect `add([1, 2, 3])` to return 6
2. Expect `add(["1", "2", "3"])` to return an error
3. Expect `add([1, 2, -3])` return 0
4. Expect `add()` to return 0

# Functional Test

When a user creates a new account they must provide an email and password. The email must be valid and the password must have at least 8 characters and contain at least 1 special character (!,@,# etc) and 1 number. If they don't provide a valid email or password then they are shown an error message.

## Expectations:

- The email provided should be valid
  - valid email = string containing `@`
- The password provided by user is valid
  - valid password >= 8 characters in length, contains 1 special character (!,@,# etc), and at least 1 number
- Password should have 8 or greater characters
- Should through an error if the user doesn't provide a valid password or valid email
- If a user enters 10 characters as a password with a valid email, they are able to create an account.
- If a user provides an email with too many `@`, they will see an error.

## Test Specs

Funtional test specifications should take the form of: (GIVEN) some context. (WHEN) some action is carried out. (THEN) a particular set of observable consequences should obtain

GIVEN I am a new user visiting the site

WHEN I naviagte to the signup page
THEN I see a form to enter my email and password.

WHEN I enter only a valid email AND click the submit button
THEN I see an error message.

WHEN I enter only a valid password AND click the submit button
THEN I see an error messahe.
