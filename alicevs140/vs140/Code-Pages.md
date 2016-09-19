---
title: "Code Pages"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4a26fc42-185a-4add-98bf-a7b314ae6186
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Code Pages
A `code page` is a character set, which can include numbers, punctuation marks, and other glyphs. Different languages and locales may use different code pages. For example, ANSI code page 1252 is used for English and most European languages; OEM code page 932 is used for Japanese Kanji.  
  
 A code page can be represented in a table as a mapping of characters to single-byte values or multibyte values. Many code pages share the ASCII character set for characters in the range 0x00 – 0x7F.  
  
 The Microsoft run-time library uses the following types of code pages:  
  
-   System-default ANSI code page. By default, at startup the run-time system automatically sets the multibyte code page to the system-default ANSI code page, which is obtained from the operating system. The call:  
  
    ```  
    setlocale ( LC_ALL, "" );  
    ```  
  
     also sets the locale to the system-default ANSI code page.  
  
-   Locale code page. The behavior of a number of run-time routines is dependent on the current locale setting, which includes the locale code page. (For more information, see [Locale-Dependent Routines](../vs140/Locale.md).) By default, all locale-dependent routines in the Microsoft run-time library use the code page that corresponds to the "C" locale. At run-time you can change or query the locale code page in use with a call to [setlocale](../vs140/setlocale--_wsetlocale.md).  
  
-   Multibyte code page. The behavior of most of the multibyte-character routines in the run-time library depends on the current multibyte code page setting. By default, these routines use the system-default ANSI code page. At run-time you can query and change the multibyte code page with [_getmbcp](../vs140/_getmbcp.md) and [_setmbcp](../vs140/_setmbcp.md), respectively.  
  
-   The "C" locale is defined by ANSI to correspond to the locale in which C programs have traditionally executed. The code page for the "C" locale ("C" code page) corresponds to the ASCII character set. For example, in the "C" locale, `islower` returns true for the values 0x61 – 0x7A only. In another locale, `islower` may return true for these as well as other values, as defined by that locale.  
  
## See Also  
 [Internationalization](../vs140/Internationalization.md)   
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)