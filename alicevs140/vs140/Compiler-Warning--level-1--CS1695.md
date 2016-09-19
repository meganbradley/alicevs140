---
title: "Compiler Warning (level 1) CS1695"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc4e4d00-0618-400d-985b-90968e98772c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1695
Invalid #pragma checksum syntax; should be #pragma checksum "filename" "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}" "XXXX..."  
  
 You should rarely encounter this error since the checksum is generally inserted at run time if you are generating code by means of the Code Dom API.  
  
 However, if you were to type in this `#pragma` statement and mistype either the GUID or checksum, you would get this error. The syntax checking by the compiler does not validate that you typed in a correct GUID, but it does check for the right number of digits and delimiters, and that the digits are hexadecimal. Likewise, it verifies that the checksum contains an even number of digits, and that the digits are hexadecimal.  
  
## Example  
 The following example generates CS1695.  
  
```  
// CS1695.cs  
  
#pragma checksum "12345"  // CS1695  
  
public class Test  
{  
    static void Main()  
    {  
    }  
}  
```