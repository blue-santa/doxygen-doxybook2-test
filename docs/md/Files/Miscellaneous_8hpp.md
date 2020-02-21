---
title: Miscellaneous.hpp


---

# Miscellaneous.hpp










## Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[testUserInput](Files/Miscellaneous_8hpp.md#function-testuserinput)**(string & user_input_temp, int & userInput)  |
| void | **[capture_user_input](Files/Miscellaneous_8hpp.md#function-capture_user_input)**(int & userInput)  |
| void | **[waitForContinue](Files/Miscellaneous_8hpp.md#function-waitforcontinue)**()  |
| void | **[clearConsole](Files/Miscellaneous_8hpp.md#function-clearconsole)**()  |







## Functions Documentation

### function testUserInput

```cpp
bool testUserInput(
    string & user_input_temp,
    int & userInput
)
```




























### function capture_user_input

```cpp
void capture_user_input(
    int & userInput
)
```




























### function waitForContinue

```cpp
void waitForContinue()
```




























### function clearConsole

```cpp
void clearConsole()
```
































## Source code

```cpp
/*
 * Miscellaneous.hpp
 * CS 201
 * December 7, 2019
 * Bryan Beus
 * Declaration file for miscellaneous content
 */

#ifndef MISC_HPP
#define MISC_HPP 

#include <iostream>
#include <iomanip>
#include <vector>
#include <string>

using std::vector;
using std::string;
using std::cout;
using std::cin;
using std::endl;
using std::getline;
using std::istringstream;
using std::setw;
using std::left;

// Clear the console
void clearConsole();

// Wait for user response
void waitForContinue();

// Capture the user input
void capture_user_input(int& userInput);

// Test whether the user's integer input is a valid response
bool testUserInput(string& user_input_temp, int& userInput);

#endif
```


-------------------------------

Updated on 20 February 2020 at 22:35:52 AKST
