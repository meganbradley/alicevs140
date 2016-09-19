---
title: "ctype&lt;char&gt; Class"
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
ms.assetid: ee30acb4-a743-405e-b3d4-13602092da84
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ctype&lt;char&gt; Class
The class is an explicit specialization of template class **ctype<CharType**> to type `char`, describing an object that can serve as a locale facet to characterize various properties of a character of type `char`.  
  
## Syntax  
  
```  
template<> class ctype<char>  
    : public ctype_base  
{  
public:  
    typedef char _Elem;  
    typedef _Elem char_type;  
    bool is(  
        mask _Maskval,  
        _Elem _Ch  
    ) const;  
    const _Elem* is(  
        const _Elem * _First,  
        const _Elem * _Last,  
        mask * _Dest  
    ) const;  
    const _Elem* scan_is(  
        mask _Maskval,  
        const _Elem * _First,  
        const _Elem * _Last  
    ) const;  
    const _Elem* scan_not(  
        mask _Maskval,  
        const _Elem * _First,  
        const _Elem * _Last  
    ) const;  
    _Elem tolower(  
        _Elem _Ch  
    ) const;  
    const _Elem* tolower(  
        _Elem * _First,  
        const _Elem * _Last  
    ) const;  
    _Elem toupper(  
        _Elem _Ch  
    ) const;  
    const _Elem* toupper(  
        _Elem * _First,  
        const _Elem * _Last  
    ) const;  
    _Elem widen(  
        char _Byte  
    ) const;  
    const _Elem* widen(  
        const char * _First,  
        const char * _Last,  
        _Elem * _Dest  
    ) const;  
    const _Elem* _Widen_s(  
        const char * _First,  
        const char * _Last,  
        _Elem * _Dest,  
        size_t _Dest_size  
    ) const;  
    _Elem narrow(  
        _Elem _Ch,  
        char _Dflt = '\0'  
    ) const;  
    const _Elem* narrow(  
        const _Elem * _First,  
        const _Elem * _Last,  
        char _Dflt,  
        char * _Dest  
    ) const;  
    const _Elem* _Narrow_s(  
        const _Elem * _First,  
        const _Elem * _Last,  
        char _Dflt,  
        char * _Dest,  
        size_t _Dest_size  
    ) const;  
    static locale::id& id;  
    explicit  ctype(  
        const mask * _Table = 0,  
        bool _Deletetable = false,  
        size_t _Refs = 0);  
protected:  
    virtual  ~ctype();  
    //other protected members  
};  
```  
  
## Remarks  
 The explicit specialization differs from the template class in several ways:  
  
-   An object of class ctype< `char`> stores a pointer to the first element of a ctype mask table, an array of UCHAR_MAX + 1 elements of type **ctype_base::mask**. It also stores a Boolean object that indicates whether the array should be deleted (using `operator delete[]`) when the ctype< **Elem**> object is destroyed.  
  
-   Its sole public constructor lets you specify **tab**, the ctype mask table, and **del**, the Boolean object that is true if the array should be deleted when the ctype< `char`> object is destroyed, as well as the reference-count parameter refs.  
  
-   The protected member function **table** returns the stored ctype mask table.  
  
-   The static member object **table_size** specifies the minimum number of elements in a ctype mask table.  
  
-   The protected static member function **classic_table**( returns the ctype mask table appropriate to the "C" locale.  
  
-   There are no protected virtual member functions [do_is](../vs140/ctype-Class.md#ctype__do_is), [do_scan_is](../vs140/ctype-Class.md#ctype__do_scan_is), or [do_scan_not](../vs140/ctype-Class.md#ctype__do_scan_not). The corresponding public member functions perform the equivalent operations themselves.  
  
 The member functions [do_narrow](../vs140/ctype-Class.md#ctype__do_narrow) and [do_widen](../vs140/ctype-Class.md#ctype__do_widen) copy elements unaltered.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [facet Class](7dd6d271-472d-4750-8fb5-ea8f55fbef62locale_class)   
 [ctype_base Class](../vs140/ctype_base-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)