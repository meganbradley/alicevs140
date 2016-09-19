---
title: "&lt;locale&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ca56f9d2-7128-44da-8df1-f4c78c17fbf2
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;locale&gt;
Defines template classes and functions that C++ programs can use to encapsulate and manipulate different cultural conventions regarding the representation and formatting of numeric, monetary, and calendric data, including internationalization support for character classification and string collation.  
  
## Syntax  
  
```  
#include <locale>  
  
```  
  
### Functions  
  
|||  
|-|-|  
|[has_facet](../vs140/-locale--functions.md#has_facet)|Tests if a particular facet is stored in a specified locale.|  
|[isalnum](../vs140/-locale--functions.md#isalnum)|Tests whether an element in a locale is an alphabetic or a numeric character.|  
|[isalpha](../vs140/-locale--functions.md#isalpha)|Tests whether an element in a locale is alphabetic character.|  
|[iscntrl](../vs140/-locale--functions.md#iscntrl)|Tests whether an element in a locale is a control character.|  
|[isdigit](../vs140/-locale--functions.md#isdigit)|Tests whether an element in a locale is a numeric character.|  
|[isgraph](../vs140/-locale--functions.md#isgraph)|Tests whether an element in a locale is an alphanumeric or punctuation character.|  
|[islower](../vs140/-locale--functions.md#islower)|Tests whether an element in a locale is lower case.|  
|[isprint](../vs140/-locale--functions.md#isprint)|Tests whether an element in a locale is a printable character.|  
|[ispunct](../vs140/-locale--functions.md#ispunct)|Tests whether an element in a locale is a punctuation character.|  
|[isspace](../vs140/-locale--functions.md#isspace)|Tests whether an element in a locale is a whitespace character.|  
|[isupper](../vs140/-locale--functions.md#isupper)|Tests whether an element in a locale is upper case.|  
|[isxdigit](../vs140/-locale--functions.md#isxdigit)|Tests whether an element in a locale is a character used to represent a hexadecimal number.|  
|[tolower](../vs140/-locale--functions.md#tolower)|Converts a character to lower case.|  
|[toupper](../vs140/-locale--functions.md#toupper)|Converts a character to upper case.|  
|[use_facet](../vs140/-locale--functions.md#use_facet)|Returns a reference to a facet of a specified type stored in a locale.|  
  
### Classes  
  
|||  
|-|-|  
|[codecvt](../vs140/codecvt-Class.md)|A template class that provides a facet used to convert between internal and external character encodings.|  
|[codecvt_base](../vs140/codecvt_base-Class.md)|A base class for the codecvt class that is used to define an enumeration type referred to as **result**, used as the return type for the facet member functions to indicate the result of a conversion.|  
|[codecvt_byname](../vs140/codecvt_byname-Class.md)|A derived template class that describes an object that can serve as a collate facet of a given locale, enabling the retrieval of information specific to a cultural area concerning conversions.|  
|[collate](../vs140/collate-Class.md)|A collate template class that provides a facet that handles string sorting conventions.|  
|[collate_byname](../vs140/collate_byname-Class.md)|A derived template class that describes an object that can serve as a collate facet of a given locale, enabling the retrieval of information specific to a cultural area concerning string sorting conventions.|  
|[ctype](../vs140/ctype-Class.md)|A template class that provides a facet that is used to classify characters, convert from upper- and lowercase and between the native character set and that set used by the locale.|  
|[ctype<char\>](../vs140/ctype-char--Class.md)|A class that is an explicit specialization of template class **ctype<CharType**> to type `char`, describing an object that can serve as a locale facet to characterize various properties of a character of type `char`.|  
|[ctype_base](../vs140/ctype_base-Class.md)|A base class for the ctype class that is used to define enumeration types used to classify or test characters either individually or within entire ranges.|  
|[ctype_byname](../vs140/ctype_byname-Class.md)|A derived template class that describes an object that can serve as a ctype facet of a given locale, enabling the classification of characters and conversion of characters between case and native and locale specified character sets.|  
|[locale](../vs140/locale-Class.md)|A class that describes a locale object that encapsulates culture-specific information as a set of facets that collectively define a specific localized environment.|  
|[messages](../vs140/messages-Class.md)|A template class that describes an object that can serve as a locale facet to retrieve localized messages from a catalog of internationalized messages for a given locale.|  
|[messages_base](../vs140/messages_base-Class.md)|A base class that describes an `int` type for the catalog of messages.|  
|[messages_byname](../vs140/messages_byname-Class.md)|A derived template class that describes an object that can serve as a message facet of a given locale, enabling the retrieval of localized messages.|  
|[money_base](../vs140/money_base-Class.md)|A base class for the ctype class that is used to define enumeration types used to classify or test characters either individually or within entire ranges.|  
|[money_get](../vs140/money_get-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of sequences of type **CharType** to monetary values.|  
|[money_put](../vs140/money_put-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of monetary values to sequences of type **CharType**.|  
|[moneypunct](../vs140/moneypunct-Class.md)|A template class that describes an object that can serve as a locale facet to describe the sequences of type **CharType** used to represent a monetary input field or a monetary output field.|  
|[moneypunct_byname](../vs140/moneypunct_byname-Class.md)|A derived template class that describes an object that can serve as a moneypunct facet of a given locale enabling the formatting monetary input or output fields.|  
|[num_get](../vs140/num_get-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of sequences of type **CharType** to numeric values.|  
|[num_put](../vs140/num_put-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of numeric values to sequences of type **CharType**.|  
|[numpunct](../vs140/numpunct-Class.md)|A template class that describes an object that can serve as a local facet to describe the sequences of type **CharType** used to represent information about the formatting and punctuation of numeric and Boolean expressions.|  
|[numpunct_byname](../vs140/numpunct_byname-Class.md)|A derived template class that describes an object that can serve as a moneypunct facet of a given locale enabling the formatting and punctuation of numeric and Boolean expressions.|  
|[time_base](../vs140/time_base-Class.md)|A class that serves as a base class for facets of template class time_get, defining just the enumerated type dateorder and several constants of this type.|  
|[time_get](../vs140/time_get-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of sequences of type **CharType** to time values.|  
|[time_get_byname](../vs140/time_get_byname-Class.md)|A derived template class that describes an object that can serve as a locale facet of type time_get<**CharType**, **InputIterator**>.|  
|[time_put](../vs140/time_put-Class.md)|A template class that describes an object that can serve as a locale facet to control conversions of time values to sequences of type **CharType**.|  
|[time_put_byname](../vs140/time_put_byname-Class.md)|A derived template class that describes an object that can serve as a locale facet of type `time_put`<**CharType**, **OutputIterator**>.|  
|[wbuffer_convert Class](../vs140/wbuffer_convert-Class.md)|Describes a stream buffer that controls the transmission of elements to and from a byte stream buffer.|  
|[wstring_convert Class](../vs140/wstring_convert-Class.md)|A template class that performs conversions between a wide string and a byte string.|  
  
## See Also  
 [Code Pages](../vs140/Code-Pages.md)   
 [Locale Names, Languages, and Country/Region Strings](../vs140/Locale-Names--Languages--and-Country-Region-Strings.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)