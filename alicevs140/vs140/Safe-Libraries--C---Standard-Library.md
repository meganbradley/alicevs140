---
title: "Safe Libraries: C++ Standard Library"
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
ms.assetid: 3993340f-1f29-4d81-b3f5-52a52bc8e148
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Safe Libraries: C++ Standard Library
Several enhancements have been made to the libraries that ship with Visual C++, including the Standard C++ Library, to make them more secure.  
  
 Several methods in the Standard C++ Library have been identified as potentially unsafe because they could lead to a buffer overrun or other code defect. The use of these methods is discouraged, and new, more secure methods have been created to replace them. These new methods all end in `_s`.  
  
 Several enhancements have also been made to make iterators and algorithms more secure. For more information, see [Checked Iterators](../vs140/Checked-Iterators.md), [Debug Iterator Support](../vs140/Debug-Iterator-Support.md) and [_ITERATOR_DEBUG_LEVEL](../vs140/_ITERATOR_DEBUG_LEVEL.md).  
  
## Remarks  
 The following table lists the Standard C++ Library methods that are potentially unsafe, as well as their safer equivalent:  
  
|Potentially unsafe method|Safer equivalent|  
|-------------------------------|----------------------|  
|[basic_string::copy](../vs140/basic_string--copy.md)|[basic_string::_Copy_s](../vs140/basic_string--_Copy_s.md)|  
|[char_traits::copy](../vs140/char_traits--copy.md)|[char_traits::_Copy_s](../vs140/char_traits--_Copy_s.md)|  
  
 If you call any one of the potentially unsafe methods above, or if you use iterators incorrectly, the compiler will generate [Compiler Warning (level 1) C4996](../vs140/Compiler-Warning--level-3--C4996.md). For information on how to disable these warnings, see [_SCL_SECURE_NO_WARNINGS](../vs140/_SCL_SECURE_NO_WARNINGS.md).  
  
## In This Section  
 [_ITERATOR_DEBUG_LEVEL](../vs140/_ITERATOR_DEBUG_LEVEL.md)  
  
 [_SCL_SECURE_NO_WARNINGS](../vs140/_SCL_SECURE_NO_WARNINGS.md)  
  
 [Checked Iterators](../vs140/Checked-Iterators.md)  
  
 [Debug Iterator Support](../vs140/Debug-Iterator-Support.md)  
  
## See Also  
 [Standard C++ Library Overview](../vs140/C---Standard-Library-Overview.md)