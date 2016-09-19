---
title: "collate Class"
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
ms.assetid: 92168798-9628-4a2e-be6e-fa62dcd4d6a6
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collate Class
A template class that describes an object that can serve as a locale facet to control the ordering and grouping of characters within a string, comparisons between them and the hashing of strings.  
  
## Syntax  
  
```  
template <class CharType >  
   class collate : public locale::facet;  
```  
  
#### Parameters  
 `CharType`  
 The type used within a program to encode characters.  
  
## Remarks  
 As with any locale facet, the static object ID has an initial stored value of zero. The first attempt to access its stored value stores a unique positive value in  **id.** In some languages, characters are grouped and treated as a single character, and in others, individual characters are treated as if they were two characters. The collating services provided by the collate class provide the way to sort these cases.  
  
### Constructors  
  
|||  
|-|-|  
|[collate](#collate__collate)|The constructor for objects of class `collate` that serves as a locale facet to handle string sorting conventions.|  
  
### Typedefs  
  
|||  
|-|-|  
|[char_type](#collate__char_type)|A type that describes a character of type `CharType`.|  
|[string_type](#collate__string_type)|A type that describes a string of type `basic_string` containing characters of type `CharType`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[compare](#collate__compare)|Compares two character sequences according to their facet-specific rules for equality or inequality.|  
|[do_compare](#collate__do_compare)|A virtual function called to compare two character sequences according to their facet-specific rules for equality or inequality.|  
|[do_hash](#collate__do_hash)|A virtual function called to determine the hash value of sequences according to their facet-specific rules.|  
|[do_transform](#collate__do_transform)|A virtual function called to convert a character sequence from a locale to a string that may be used in lexicographical comparisons with other character sequences similarly converted from the same locale.|  
|[hash](#collate__hash)|Determines the hash value of sequence according to their facet-specific rules.|  
|[transform](#collate__transform)|Converts a character sequence from a locale to a string that may be used in lexicographical comparisons with other character sequences similarly converted from the same locale.|  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
##  <a name="collate__char_type"></a>  collate::char_type  
 A type that describes a character of type **CharType**.  
  
```  
typedef CharType char _ type;  
  
```  
  
### Remarks  
 The type is a synonym for the template parameter **CharType**.  
  
##  <a name="collate__collate"></a>  collate::collate  
 The constructor for objects of class collate that serves as a locale facet to handle string sorting conventions.  
  
```  
public:  
    explicit collate(  
        size_t _ Refs = 0  
    );  
protected:  
    collate(  
        const char * _Locname,  
        size_t _Refs = 0  
    );  
```  
  
### Parameters  
 `_Refs`  
 Integer value used to specify the type of memory management for the object.  
  
 `_Locname`  
 The name of the locale.  
  
### Remarks  
 The possible values for the `_Refs` parameter and their significance are:  
  
-   0: The lifetime of the object is managed by the locales that contain it.  
  
-   1: The lifetime of the object must be manually managed.  
  
-   \> 0: These values are not defined.  
  
 The constructor initializes its base object with **locale::**[facet](../vs140/locale-Class.md#facet_class)( `_Refs`).  
  
##  <a name="collate__compare"></a>  collate::compare  
 Compares two character sequences according to their facet-specific rules for equality or inequality.  
  
```  
int compare(    const CharType*  _First1 ,    const CharType*  _Last1,    const CharType*  _First2 ,    const CharType*  _Last2 ) const;  
  
```  
  
### Parameters  
 `_First1`  
 Pointer to the first element in the first sequence to be compared.  
  
 `_Last1`  
 Pointer to the last element in the first sequence to be compared.  
  
 `_First2`  
 Pointer to the first element in the second sequence to be compared.  
  
 `_Last2`  
 Pointer to the last element in the second sequence to be compared.  
  
### Return Value  
 The member function returns:  
  
-   –1 if the first sequence compares less than the second sequence.  
  
-   +1 if the second sequence compares less than the first sequence.  
  
-   0 if the sequences are equivalent.  
  
### Remarks  
 The first sequence compares less if it has the smaller element in the earliest unequal pair in the sequences, or, if no unequal pairs exist, but the first sequence is shorter.  
  
 The member function returns [do_compare](#collate__do_compare)( `_First1`, `_Last1`, `_First2`, `_Last2`).  
  
### Example  
  
```  
// collate_compare.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <tchar.h>  
using namespace std;  
  
int main() {  
   locale loc ( "German_germany" );  
   _TCHAR * s1 = _T("Das ist wei\x00dfzz."); // \x00df is the German sharp-s, it comes before z in the German alphabet  
   _TCHAR * s2 = _T("Das ist weizzz.");  
   int result1 = use_facet<collate<_TCHAR> > ( loc ).  
      compare ( s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );  
   cout << result1 << endl;  
  
   locale loc2 ( "C" );  
   int result2 = use_facet<collate<_TCHAR> > ( loc2 ).  
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );  
   cout << result2 << endl;  
}  
```  
  
##  <a name="collate__do_compare"></a>  collate::do_compare  
 A virtual function called to compare two character sequences according to their facet-specific rules for equality or inequality.  
  
```  
virtual int do _ compare(    const CharType*  _First1 ,    const CharType*  _Last1,    const CharType*  _First2 ,    const CharType*  _Last2 ) const;  
  
```  
  
### Parameters  
 `_First1`  
 Pointer to the first element in the first sequence to be compared.  
  
 `_Last1`  
 Pointer to the last element in the first sequence to be compared.  
  
 `_First2`  
 Pointer to the first element in the second sequence to be compared.  
  
 `_Last2`  
 Pointer to the last element in the second sequence to be compared.  
  
### Return Value  
 The member function returns:  
  
-   -1 if the first sequence compares less than the second sequence.  
  
-   +1 if the second sequence compares less than the first sequence.  
  
-   0 if the sequences are equivalent.  
  
### Remarks  
 The protected virtual member function compares the sequence at [                        *_First1, Last1)* with the sequence at                         *[_First2, _Last2*). It compares values by applying **operator<** between pairs of corresponding elements of type **CharType**. The first sequence compares less if it has the smaller element in the earliest unequal pair in the sequences or if no unequal pairs exist but the first sequence is shorter.  
  
### Example  
  See the example for [collate::compare](#collate__compare), which calls `do_compare`.  
  
##  <a name="collate__do_hash"></a>  collate::do_hash  
 A virtual function called to determine the hash value of sequences according to their facet-specific rules.  
  
```  
virtual long do _ hash(    const CharType*  _First ,    const CharType*  _Last ) const;  
  
```  
  
### Parameters  
 `_First`  
 A pointer to the first character in the sequence whose has value is to be determined.  
  
 `_Last`  
 A pointer to the last character in the sequence whose has value is to be determined.  
  
### Return Value  
 A hash value of type **long** for the sequence.  
  
### Remarks  
 A hash value can be useful, for example, in distributing sequences pseudo-randomly across an array of lists.  
  
### Example  
  See the example for [hash](#collate__hash), which calls `do_hash`.  
  
##  <a name="collate__do_transform"></a>  collate::do_transform  
 A virtual function called to convert a character sequence from a locale to a string that may be used in lexicographical comparisons with other character sequences similarly converted from the same locale.  
  
```  
virtual string _ type do _ transform(    const CharType*  _First ,    const CharType*  _Last ) const;  
  
```  
  
### Parameters  
 `_First`  
 A pointer to the first character in the sequence to be converted.  
  
 `_Last`  
 A pointer to the last character in the sequence to be converted.  
  
### Return Value  
 A string that is the transformed character sequence.  
  
### Remarks  
 The protected virtual member function returns an object of class [string_type](#collate__string_type) whose controlled sequence is a copy of the sequence [ `_First`, `_Last`). If a class derived from collate< **CharType**> overrides [do_compare](#collate__do_compare), it should also override `do_transform` to match. When passed to `collate::compare`, two transformed strings should yield the same result that you would get from passing the untransformed strings to compare in the derived class.  
  
### Example  
  See the example for [transform](#collate__transform), which calls `do_transform`.  
  
##  <a name="collate__hash"></a>  collate::hash  
 Determines the hash value of sequence according to their facet-specific rules.  
  
```  
long hash(    const CharType*  _First ,    const CharType*  _Last ) const;  
  
```  
  
### Parameters  
 `_First`  
 A pointer to the first character in the sequence whose has value is to be determined.  
  
 `_Last`  
 A pointer to the last character in the sequence whose has value is to be determined.  
  
### Return Value  
 A hash value of type **long** for the sequence.  
  
### Remarks  
 The member function returns [do_hash](#collate__do_hash)( `_First`, `_Last`).  
  
 A hash value can be useful, for example, in distributing sequences pseudo-randomly across an array of lists.  
  
### Example  
  
```  
// collate_hash.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <tchar.h>  
using namespace std;  
  
int main( )     
{  
   locale loc ( "German_germany" );  
   _TCHAR * s1 = _T("\x00dfzz abc."); // \x00df is the German sharp-s (looks like beta), it comes before z in the alphabet  
   _TCHAR * s2 = _T("zzz abc."); // \x00df is the German sharp-s (looks like beta), it comes before z in the alphabet  
  
   long r1 = use_facet< collate<_TCHAR> > ( loc ).  
      hash (s1, &s1[_tcslen( s1 )-1 ]);  
   long r2 =  use_facet< collate<_TCHAR> > ( loc ).  
      hash (s2, &s2[_tcslen( s2 )-1 ] );  
   cout << r1 << " " << r2 << endl;  
}  
```  
  
  **541187293 551279837**    
##  <a name="collate__string_type"></a>  collate::string_type  
 A type that describes a string of type `basic_string` containing characters of type **CharType**.  
  
```  
typedef basic _ string<CharType> string _ type;  
  
```  
  
### Remarks  
 The type describes a specialization of template class [basic_string](../vs140/basic_string-Class.md) whose objects can store copies of the source sequence.  
  
### Example  
  For an example of how to declare and use `string_type`, see [transform](#collate__transform).  
  
##  <a name="collate__transform"></a>  collate::transform  
 Converts a character sequence from a locale to a string that may be used in lexicographical comparisons with other character sequences similarly converted from the same locale.  
  
```  
string _ type transform(    const CharType*  _First ,    const CharType*  _Last ) const;  
  
```  
  
### Parameters  
 `_First`  
 A pointer to the first character in the sequence to be converted.  
  
 `_Last`  
 A pointer to the last character in the sequence to be converted.  
  
### Return Value  
 A string that contains the transformed character sequence.  
  
### Remarks  
 The member function returns [do_transform](#collate__do_transform)( `_First`, `_Last`).  
  
### Example  
  
```  
// collate_transform.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <tchar.h>  
using namespace std;  
  
int main( )     
{  
   locale loc ( "German_Germany" );  
   _TCHAR* s1 = _T("\x00dfzz abc.");   
   // \x00df is the German sharp-s (looks like beta),   
   // it comes before z in the alphabet  
   _TCHAR* s2 = _T("zzz abc.");   
  
   collate<_TCHAR>::string_type r1;   // OK for typedef?  
   r1 = use_facet< collate<_TCHAR> > ( loc ).  
      transform (s1, &s1[_tcslen( s1 )-1 ]);  
  
   cout << r1 << endl;  
  
   basic_string<_TCHAR> r2 = use_facet< collate<_TCHAR> > ( loc ).  
      transform (s2, &s2[_tcslen( s2 )-1 ]);  
  
   cout << r2 << endl;  
  
   int result1 = use_facet<collate<_TCHAR> > ( loc ).compare   
      (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );  
  
   cout << _tcscmp(r1.c_str( ),r2.c_str( )) << result1   
      << _tcscmp(s1,s2) <<endl;  
}  
```  
  
  **????????    ?**  
**????**  
**???????      ?**  
**????**  
**-1-11**    
## See Also  
 [<locale\>](../vs140/-locale-.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)