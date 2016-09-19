---
title: "Support for Multibyte Character Sets (MBCSs)"
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
ms.assetid: b498733c-a1e1-45e3-8f26-d6da3cb5f2dd
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Support for Multibyte Character Sets (MBCSs)
Multibyte character sets (MBCSs) are an older approach to the need to support character sets, like Japanese and Chinese, that cannot be represented in a single byte. If you are doing new development, you should use Unicode for all text strings except perhaps system strings that are not seen by end users. MBCS is a legacy technology and is not recommended for new development.  
  
 The most common MBCS implementation is double-byte character sets (DBCSs). Visual C++ in general, and MFC in particular, is fully enabled for DBCS.  
  
> [!WARNING]
>  In Visual Studio 2013 and later, the MFC libraries for multi-byle character encoding (MBCS) will be provided as an add-on to Visual Studio and will be available free of charge to Visual Studio customers (Professional and Enterprise editions only) from the MSDN download site.  
>   
>  The libraries require about 440 MB on your drive, and the installation includes all localized versions of the libraries. You can install it on any machine on which Visual Studio Community, Professional, or Enterprise edition is installed, and which has the in-box MFC feature enabled.  
>   
>  If you uninstall or repair Visual Studio, the MBCS libraries will also be uninstalled or repaired. However, if you just remove the MFC feature, the MBCS libraries will remain on your system. If you repair the MBCS libraries, Visual Studio is not modified in any way.  
>   
>  The Redistributable Packages for Visual Studio 2013 and later will still include the MBCS MFC DLLs. No additional steps are required to redistribute the DLLs to your customers.  
  
 For samples, see the MFC source code files.  
  
 For platforms used in markets whose languages use large character sets, the best alternative to Unicode is MBCS. MFC supports MBCS by using internationalizable data types and C run-time functions. You should do the same in your code.  
  
 Under MBCS, characters are encoded in either 1 or 2 bytes. In 2-byte characters, the first, or lead byte, signals that both it and the following byte are to be interpreted as one character. The first byte comes from a range of codes reserved for use as lead bytes. Which ranges of bytes can be lead bytes depends on the code page in use. For example, Japanese code page 932 uses the range 0x81 through 0x9F as lead bytes, but Korean code page 949 uses a different range.  
  
 Consider all the following in your MBCS programming.  
  
 MBCS characters in the environment  
 MBCS characters can appear in strings such as file and directory names.  
  
 Editing operations  
 Editing operations in MBCS applications should operate on characters, not bytes. The caret should not split a character, the RIGHT ARROW key should move right one character, and so on. **Delete** should delete a character; **Undo** should reinsert it.  
  
 String handling  
 In an application that uses MBCS, string handling poses special problems. Characters of both widths are mixed in a single string; therefore, you must remember to check for lead bytes.  
  
 Run-time library support  
 The C run-time library and MFC support single-byte, MBCS, and Unicode programming. Single-byte strings are processed with the `str` family of run-time functions, MBCS strings are processed with corresponding `_mbs` functions, and Unicode strings are processed with corresponding *wcs* functions. MFC class member function implementations use portable run-time functions that map, under the right circumstances, to the normal `str` family of functions, the MBCS functions, or the Unicode functions, as described in "MBCS/Unicode portability."  
  
 MBCS/Unicode portability  
 Using the Tchar.h header file, you can build single-byte, MBCS, and Unicode applications from the same sources. Tchar.h defines macros prefixed with *_tcs* , which map to `str`, `_mbs`, or *wcs* functions, as appropriate. To build MBCS, define the symbol **_MBCS**. To build Unicode, define the symbol **_UNICODE**. By default, **_MBCS** is defined for MFC applications. For more information, see [Generic-Text Mappings in Tchar.h](../vs140/Generic-Text-Mappings-in-Tchar.h.md).  
  
> [!NOTE]
>  Behavior is undefined if you define both **_UNICODE** and **_MBCS**.  
  
 The Mbctype.h and Mbstring.h header files define MBCS-specific functions and macros, which you might need in some cases. For example, `_ismbblead` tells you whether a specific byte in a string is a lead byte.  
  
 For international portability, code your program with [Unicode](../vs140/Support-for-Unicode.md) or multibyte character sets (MBCSs).  
  
## What do you want to do?  
  
-   [Enable MBCS in my program](../vs140/International-Enabling.md)  
  
-   [Enable both Unicode and MBCS in my program](../vs140/Internationalization-Strategies.md)  
  
-   [Use MBCS to create an internationalized program](../vs140/MBCS-Programming-Tips.md)  
  
-   [See a summary of MBCS programming](../vs140/MBCS-Programming-Tips.md)  
  
-   [Learn about generic-text mappings for byte-width portability](../vs140/Generic-Text-Mappings-in-Tchar.h.md)  
  
## See Also  
 [Text and Strings](../vs140/Text-and-Strings-in-Visual-C--.md)   
 [MBCS Support in Visual C++](../vs140/MBCS-Support-in-Visual-C--.md)