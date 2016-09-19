---
title: "&lt;string&gt; typedefs"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdca01e9-f2f1-4b59-abda-0093d760b3cc
caps.latest.revision: 12
---
# &lt;string&gt; typedefs
||||  
|-|-|-|  
|[string](#string)|[u16string](#u16string)|[u32string](#u32string)|  
|[wstring](#wstring)|  
  
##  <a name="string"></a>  string  
 A type that describes a specialization of the template class [basic_string](../vs140/basic_string-Class.md) with elements of type `char`.  
  
 Other typedefs that specialize `basic_string` include [wstring](../vs140/-string--typedefs.md#wstring), [u16string](../vs140/-string--typedefs.md#u16string), and [u32string](../vs140/-string--typedefs.md#u32string).  
  
```cpp  
typedef basic_string<char, char_traits<char>, allocator<char>> string;  
```  
  
### Remarks  
 The following are equivalent declarations:  
  
```cpp  
string str("");  
  
basic_string<char> str("");  
```  
  
 For a list of string constructors, see [basic_string::basic_string](../vs140/basic_string-Class.md#basic_string__basic_string).  
  
##  <a name="u16string"></a>  u16string  
 A type that describes a specialization of the template class [basic_string](../vs140/basic_string-Class.md) with elements of type `char16_t`.  
  
 Other typedefs that specialize `basic_string` include [wstring](../vs140/-string--typedefs.md#wstring), [string](../vs140/-string--typedefs.md#string), and [u32string](../vs140/-string--typedefs.md#u32string).  
  
```cpp  
typedef basic_string<char16_t, char_traits<char16_t>, allocator<char16_t>> u16string;  
```  
  
### Remarks  
 For a list of string constructors, see [basic_string::basic_string](../vs140/basic_string-Class.md#basic_string__basic_string).  
  
##  <a name="u32string"></a>  u32string  
 A type that describes a specialization of the template class [basic_string](../vs140/basic_string-Class.md) with elements of type `char32_t`.  
  
 Other typedefs that specialize `basic_string` include [string](../vs140/-string--typedefs.md#string), [u16string](../vs140/-string--typedefs.md#u16string), and [wstring](../vs140/-string--typedefs.md#wstring).  
  
```cpp  
typedef basic_string<char32_t, char_traits<char32_t>, allocator<char32_t>> u32string;  
```  
  
### Remarks  
 For a list of string constructors, see [basic_string::basic_string](../vs140/basic_string-Class.md#basic_string__basic_string).  
  
##  <a name="wstring"></a>  wstring  
 A type that describes a specialization of the template class [basic_string](../vs140/basic_string-Class.md) with elements of type `wchar_t`.  
  
 Other typedefs that specialize `basic_string` include [string](../vs140/-string--typedefs.md#string), [u16string](../vs140/-string--typedefs.md#u16string), and [u32string](../vs140/-string--typedefs.md#u32string).  
  
```cpp  
typedef basic_string<wchar_t, char_traits<wchar_t>, allocator<wchar_t>> wstring;  
```  
  
### Remarks  
 The following are equivalent declarations:  
  
```cpp  
wstring wstr(L"");  
  
basic_string<wchar_t> wstr(L"");  
```  
  
 For a list of string constructors, see [basic_string::basic_string](../vs140/basic_string-Class.md#basic_string__basic_string).  
  
> [!NOTE]
>  The size of `wchar_t` is implementation-defined. If your code depends on `wchar_t` to be a certain size, check your platform's implementation (for example, with `sizeof(wchar_t)`). If you need a string character type with a width that is guaranteed to remain the same on all platforms, use [string](../vs140/-string--typedefs.md#string), [u16string](../vs140/-string--typedefs.md#u16string), or [u32string](../vs140/-string--typedefs.md#u32string).  
  
## See Also  
 [&lt;string&gt;](../vs140/-string-.md)