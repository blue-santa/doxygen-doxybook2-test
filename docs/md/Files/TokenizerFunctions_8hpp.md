---
title: TokenizerFunctions.hpp


---

# TokenizerFunctions.hpp










## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[PrintTokens](Files/TokenizerFunctions_8hpp.md#function-printtokens)**(ostream & os, const vector< string > & tokens, const vector< pair< int, int >> & linecols)  |
| bool | **[ReadLine](Files/TokenizerFunctions_8hpp.md#function-readline)**(istream & is, vector< string > & tokens, vector< pair< int, int >> & linecols)  |
| bool | **[LineToTokens](Files/TokenizerFunctions_8hpp.md#function-linetotokens)**(const string & line, vector< string > & tokens)  |







## Functions Documentation

### function PrintTokens

```cpp
void PrintTokens(
    ostream & os,
    const vector< string > & tokens,
    const vector< pair< int, int >> & linecols
)
```




























### function ReadLine

```cpp
bool ReadLine(
    istream & is,
    vector< string > & tokens,
    vector< pair< int, int >> & linecols
)
```




























### function LineToTokens

```cpp
bool LineToTokens(
    const string & line,
    vector< string > & tokens
)
```
































## Source code

```cpp
/*
 * TokenizerFunctions.hpp
 * CS 202
 * February 15, 2020
 * Bryan Beus
 * Header definition file
 */

#ifndef __TIMEIT_FUNC__
#define __TIMEIT_FUNC__

#include <random>
#include <vector>

#include "StopWatch.hpp"

using std::vector;
using std::string;
using std::istream;
using std::pair;
using std::ostream;

// Convert lines to tokens
bool LineToTokens(const string& line, vector<string>& tokens);

// Read lines
bool ReadLine(istream& is, vector<string>& tokens, vector<pair<int, int>>& linecols);

// Print tokens
void PrintTokens(ostream& os, const vector<string>& tokens, const vector<pair<int, int>>& linecols);

#endif
```


-------------------------------

Updated on 20 February 2020 at 22:35:52 AKST
