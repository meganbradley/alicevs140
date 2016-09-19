---
title: "&lt;string&gt; functions"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1a4ffd11-dce5-4cc6-a043-b95de034c7c4
caps.latest.revision: 13
---
# &lt;string&gt; functions
||||  
|-|-|-|  
|[getline Template Function](#getline_template_function)|[stod](#stod)|[stof](#stof)|  
|[stoi](#stoi)|[stol](#stol)|[stold](#stold)|  
|[stoll](#stoll)|[stoul](#stoul)|[stoull](#stoull)|  
|[swap](#swap)|[to_string](#to_string)|[to_wstring](#to_wstring)|  
  
##  <a name="getline_template_function"></a>  getline Template Function  
 Extract strings from the input stream line-by-line.  
  
```  
// (1) delimiter as parameter  
template<class CharType, class Traits, class Allocator>  
basic_istream<CharType, Traits>& getline(  
    basic_istream<CharType, Traits>& is,  
    basic_string<CharType, Traits, Allocator>& str, CharType delim);  
  
template<class CharType, class Traits, class Allocator>  
basic_istream<CharType, Traits>& getline(  
    basic_istream<CharType, Traits>&& is,  
    basic_string<CharType, Traits, Allocator>& str, const CharType delim);  
  
// (2) default delimiter used  
template<class CharType, class Traits, class Allocator>  
basic_istream<CharType, Traits>& getline(  
    basic_istream<CharType, Traits>& is,  
    basic_string<CharType, Traits, Allocator>& str);  
  
template<class Allocator, class Traits, class Allocator>  
basic_istream<Allocator, Traits>& getline(  
    basic_istream<Allocator, Traits>&& is,  
    basic_string<Allocator, Traits, Allocator>& str);  
  
```  
  
### Parameters  
 `is`  
 The input stream from which a string is to be extracted.  
  
 `str`  
 The string into which are read the characters from the input stream.  
  
 `delim`  
 The line delimiter.  
  
### Return Value  
 The input stream `is`.  
  
### Remarks  
 The pair of function signatures marked `(1)` extract characters from `is` until `delim` is found, storing them in `str`.  
  
 The pair of function signatures marked `(2)` use newline as the default line delimiter and behave as **getline**( `is`, `str`, `is`. `widen`(' `\n`')).  
  
 The second function of each pair is an analog to the first one to support [rvalue references](../vs140/Lvalues-and-Rvalues--Visual-C---.md).  
  
 Extraction stops when one of the following occurs:  
  
-   At end-of-file, in which case the internal state flag of `is` is set to `ios_base::eofbit`.  
  
-   After the function extracts an element that compares equal to **delim**, in which case the element is neither put back nor appended to the controlled sequence.  
  
-   After the function extracts `str.`[max_size](../vs140/basic_string-Class.md#basic_string__max_size) elements, in which case the internal state flag of `is` is set to `ios_base::failbit`.  
  
-   Some other error other than those previously listed, in which case the internal state flag of `is` is set to `ios_base::badbit`  
  
 For information about internal state flags, see [ios_base::iostate](../vs140/ios_base-Class.md#ios_base__iostate).  
  
 If the function extracts no elements, the internal state flag of `is` is set to `ios_base::failbit`. In any case, `getline` returns `is`.  
  
 If an exception is thrown, `is` and `str` are left in a valid state.  
  
### Example  
  The following code demonstrates `getline()` in two modes: first with the default delimiter (newline) and second with a whitespace as delimiter. The end-of-file character (CTRL-Z on the keyboard) is used to control termination of the while loops. This sets the internal state flag of `cin` to `eofbit`, which must be cleared with [basic_ios::clear()](../vs140/basic_ios-Class.md#basic_ios__clear) before the second while loop will work properly.  
  
```cpp  
// compile with: /EHsc /W4  
#include <string>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main()  
{  
    string str;  
    vector<string> v1;  
    cout << "Enter a sentence, press ENTER between sentences. (Ctrl-Z to stop): " << endl;  
    // Loop until end-of-file (Ctrl-Z) is input, store each sentence in a vector.  
    // Default delimiter is the newline character.  
    while (getline(cin, str)) {  
        v1.push_back(str);  
    }  
  
    cout << "The following input was stored with newline delimiter:" << endl;  
    for (const auto& p : v1) {  
        cout << p << endl;  
    }  
  
    cin.clear();  
  
    vector<string> v2;  
    // Now try it with a whitespace delimiter  
    while (getline(cin, str, ' ')) {  
        v2.push_back(str);  
    }  
  
    cout << "The following input was stored with whitespace as delimiter:" << endl;  
    for (const auto& p : v2) {  
        cout << p << endl;  
    }  
}  
  
```  
  
##  <a name="stod"></a>  stod  
 Converts a character sequence to a `double`.  
  
```  
double stod(  
    const string& _Str,   
    size_t * _Idx = 0  
);  
double stod(  
    const wstring& _Str,   
    size_t * _Idx = 0  
;  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
  
### Return Value  
 The `double` value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `double` as if by calling `strtod(_Str.c_str(), _Eptr)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stof"></a>  stof  
 Converts a character sequence to a float.  
  
```  
float stof(  
    const string& _Str,   
    size_t * _Idx = 0  
);  
float stof(  
    const wstring& _Str,   
    size_t * _Idx = 0  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
  
### Return Value  
 The float value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `float` as if by calling `strtof(_Str.c_str(), _Eptr)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stoi"></a>  stoi  
 Converts a character sequence to an integer.  
  
```  
int stoi(  
    const string& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
int stoi(  
    const wstring& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
```  
  
### Return Value  
 The integer value.  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|Contains the index of the first unconverted character on return.|  
|`_Base`|The number base to use.|  
  
### Remarks  
 The function `stoi` converts the sequence of characters in `_Str` to a value of type `int` and returns the value. For example, when passed a character sequence "10", the value returned by `stoi` is the integer 10.  
  
 `stoi` behaves similarly to the function `strtol` for single-byte characters when it is called in the manner `strtol(_Str.c_str(), _Eptr, _Base)`, where `_Eptr` is an object internal to the function; or `wcstol` for wide characters, when it is called in similar manner, `wcstol(Str.c_str(), _Eptr, _Base)`. For more information, see [strtol, wcstol, _strtol_l, _wcstol_l](../vs140/strtol--wcstol--_strtol_l--_wcstol_l.md).  
  
 If `_Str.c_str() == *_Eptr,``stoi` throws an object of type `invalid_argument`. If such a call would set `errno`, or if the returned value cannot be represented as an object of type `int`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - __Str.c_str()` in `*_Idx`.  
  
##  <a name="stol"></a>  stol  
 Converts a character sequence to a `long`.  
  
```  
long stol(  
    const string& _Str,  
    size_t * _Idx = 0,  
    int _Base = 10  
);  
long stol(  
    const wstring& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
|`_Base`|The number base to use.|  
  
### Return Value  
 The long-integer value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `long` as if by calling `strtol(_Str.c_str(), _Eptr, _Base)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stold"></a>  stold  
 Converts a character sequence to a `long double`.  
  
```  
double stold(  
    const string& _Str,   
    size_t * _Idx = 0  
);  
double stold(  
    const wstring& _Str,   
    size_t * _Idx = 0  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
  
### Return Value  
 The `long double` value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `long double` as if by calling `strtold(_Str.c_str(), _Eptr)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stoll"></a>  stoll  
 Converts a character sequence to a `long long`.  
  
```  
long long stoll(  
    const string& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
long long stoll(  
    const wstring& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
|`_Base`|The number base to use.|  
  
### Return Value  
 The `long long` value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `long long` as if by calling `strtoll(_Str.c_str(), _Eptr, _Base)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stoul"></a>  stoul  
 Converts a character sequence to an unsigned long.  
  
```  
unsigned long stoul(  
    const string& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
unsigned long stoul(  
    const wstring& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
|`_Base`|The number base to use.|  
  
### Return Value  
 The unsigned long-integer value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `unsigned long` as if by calling `strtoul(_Str.c_str(), _Eptr, _Base)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="stoull"></a>  stoull  
 Converts a character sequence to an `unsigned long long`.  
  
```  
unsigned long long stoull(  
    const string& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
unsigned long long stoull(  
    const wstring& _Str,   
    size_t * _Idx = 0,  
    int _Base = 10  
);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Str`|The character sequence to be converted.|  
|`_Idx`|The index value of the first unconverted character.|  
|`_Base`|The number base to use.|  
  
### Return Value  
 The `unsigned long long` value.  
  
### Remarks  
 The function converts the sequence of elements in `_Str` to a value `_Val` of type `unsigned long long` as if by calling `strtoull(_Str.c_str(), _Eptr, _Base)`, where `_Eptr` is an object internal to the function. If `_Str.c_str() == *_Eptr` it throws an object of type `invalid_argument`. If such a call would set `errno`, it throws an object of type `out_of_range`. Otherwise, if `_Idx` is not a null pointer, the function stores `*_Eptr - _Str.c_str()` in `*_Idx` and returns `_Val`.  
  
##  <a name="swap"></a>  swap  
 Exchanges the arrays of characters of two strings.  
  
```  
template<class Traits, class Allocator>    void swap(       basic _ string<CharType, Traits, Allocator>&  _Left ,       basic _ string<CharType, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 One string whose elements are to be swapped with those of another string.  
  
 `_Right`  
 The other string whose elements are to be swapped with the first string.  
  
### Remarks  
 The template function executes the specialized member function _                        *Left*. [swap](../vs140/basic_string-Class.md#basic_string__swap)(\_                        *Right*) for strings, which guarantees constant complexity.  
  
### Example  
  
```  
// string_swap.cpp  
// compile with: /EHsc  
#include <string>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   // Declaring an object of type basic_string<char>  
   string s1 ( "Tweedledee" );  
   string s2 ( "Tweedledum" );  
   cout << "Before swapping string s1 and s2:" << endl;  
   cout << "The basic_string s1 = " << s1 << "." << endl;  
   cout << "The basic_string s2 = " << s2 << "." << endl;  
  
   swap ( s1 , s2 );  
   cout << "\nAfter swapping string s1 and s2:" << endl;  
   cout << "The basic_string s1 = " << s1 << "." << endl;  
   cout << "The basic_string s2 = " << s2 << "." << endl;  
}  
```  
  
  **Before swapping string s1 and s2:**  
**The basic_string s1 = Tweedledee.**  
**The basic_string s2 = Tweedledum.**  
**After swapping string s1 and s2:**  
**The basic_string s1 = Tweedledum.**  
**The basic_string s2 = Tweedledee.**    
##  <a name="to_string"></a>  to_string  
 Converts a value to a `string`.  
  
```  
string to_string(int Val);  
string to_string(unsigned int Val);  
string to_string(long Val);  
string to_string(unsigned long Val);  
string to_string(long long Val);  
string to_string(unsigned long long Val);  
string to_string(float Val);  
string to_string(double Val);  
string to_string(long double Val);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Val`|The value to be converted.|  
  
### Return Value  
 The `string` that represents the value.  
  
### Remarks  
 The function converts `Val` to a sequence of elements stored in an array object `Buf` internal to the function as if by calling `sprintf(Buf, Fmt, Val)`, where `Fmt` is  
  
-   `"%d"` if `Val` has type `int`  
  
-   `"%u"` if `Val` has type `unsigned int`  
  
-   `"%ld"` if `Val` has type `long`  
  
-   `"%lu"` if `Val` has type `unsigned long`  
  
-   `"%lld"` if `Val` has type `long long`  
  
-   `"%llu"` if `Val` has type `unsigned long long`  
  
-   `"%f"` if `Val` has type `float` or `double`  
  
-   `"%Lf"` if `Val` has type `long double`  
  
 The function returns `string(Buf)`.  
  
##  <a name="to_wstring"></a>  to_wstring  
 Converts a value to a wide string.  
  
```  
wstring to_wstring(int Val);  
wstring to_wstring(unsigned int Val);  
wstring to_wstring(long Val);  
wstring to_wstring(unsigned long Val);  
wstring to_wstring(long long Val);  
wstring to_wstring(unsigned long long Val);  
wstring to_wstring(float Val);  
wstring to_wstring(double Val);  
wstring to_wstring(long double Val);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Val`|The value to be converted.|  
  
### Return Value  
 The wide string that represents the value.  
  
### Remarks  
 The function converts `Val` to a sequence of elements stored in an array object `Buf` internal to the function as if by calling `swprintf(Buf, Len, Fmt, Val)`, where `Fmt` is  
  
-   `L"%d"` if `Val` has type `int`  
  
-   `L"%u"` if `Val` has type `unsigned int`  
  
-   `L"%ld"` if `Val` has type `long`  
  
-   `L"%lu"` if `Val` has type `unsigned long`  
  
-   `L"%lld"` if `Val` has type `long long`  
  
-   `L"%llu"` if `Val` has type `unsigned long long`  
  
-   `L"%f"` if `Val` has type `float` or `double`  
  
-   `L"%Lf"` if `Val` has type `long double`  
  
 The function returns `wstring(Buf)`.  
  
## See Also  
 [&lt;string&gt;](../vs140/-string-.md)