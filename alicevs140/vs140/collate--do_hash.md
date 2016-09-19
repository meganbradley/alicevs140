---
title: "collate::do_hash"
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
ms.assetid: 89e35b24-40a8-4085-8dce-4d4673f1739e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collate::do_hash
A virtual function called to determine the hash value of sequences according to their facet-specific rules.  
  
## Syntax  
  
```  
  
      virtual long do  
      _  
      hash(  
   const CharType* _First,  
   const CharType* _Last  
) const;  
```  
  
#### Parameters  
 `_First`  
 A pointer to the first character in the sequence whose has value is to be determined.  
  
 `_Last`  
 A pointer to the last character in the sequence whose has value is to be determined.  
  
## Return Value  
 A hash value of type **long** for the sequence.  
  
## Remarks  
 A hash value can be useful, for example, in distributing sequences pseudo-randomly across an array of lists.  
  
## Example  
 See the example for [hash](../vs140/collate--hash.md), which calls `do_hash`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [collate Class](../vs140/collate-Class.md)