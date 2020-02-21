---
title: Miscellaneous.cpp


---

# Miscellaneous.cpp










## Functions

|                | Name           |
| -------------- | -------------- |
| bool | **[testUserInput](Files/Miscellaneous_8cpp.md#function-testuserinput)**(string & user_input_temp, int & userInput)  |
| void | **[capture_user_input](Files/Miscellaneous_8cpp.md#function-capture_user_input)**(int & userInput)  |
| void | **[waitForContinue](Files/Miscellaneous_8cpp.md#function-waitforcontinue)**()  |
| void | **[clearConsole](Files/Miscellaneous_8cpp.md#function-clearconsole)**()  |







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
 * Miscellaneous.cpp
 * CS 201
 * December 7, 2019
 * Bryan Beus
 * Miscellaneous content definition file
 */

#include <iostream>
#include <iomanip>
#include <vector>
#include <string>

#include "Miscellaneous.hpp"

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
void clearConsole() {

    // Clear the console
    cout << "\033[2J\033[1;1H";
}

// Wait for user response
void waitForContinue() {
    cout << endl << "Press enter to continue...";
    getchar();
}

// Capture the user input
void capture_user_input(int& userInput) {

    // Assume user input is invalid until proven otherwise
    bool valid_input = false;

    // Initiate endless loop to wait for valid response
    while (!valid_input) {

        // Receive user input as a string
        string user_input_temp;
        cout << endl;
        cout << "Please indicate the desired temperature (celsius)." << endl;
        cout << " -- To stop the program, enter a value less than absolute zero (-274 or below))" << endl;

        getline(cin, user_input_temp);

        // Test if the user input is valid, and convert to an integer
        valid_input = testUserInput(user_input_temp, userInput);

        // If invalid, replay the while loop
        if (!valid_input) {
            cin.clear();
            cin.ignore(1000, '\n');
            cout << endl;
            cout << "Please try again" << endl;
        } 

        // Add formatting
        cout << endl;
    }
}

// Test whether the user's integer input is a valid response
bool testUserInput(string& user_input_temp, int& userInput) {

    // Assume user input is valid
    bool res = true;

    // Convert user input to an integer
    istringstream iss (user_input_temp);
    iss >> userInput;

    // If the string is not a valid reponse, return false
    if (iss.fail()) {
        res = false;
    }    

    // Return the result
    return res;
}
```


-------------------------------

Updated on 20 February 2020 at 22:35:52 AKST
