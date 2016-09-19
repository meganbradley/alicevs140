---
title: "CAtlArray::Copy"
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
ms.topic: reference
ms.assetid: 915b76ce-8a7e-41d7-9359-dc110da3ddbc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::Copy
Call this method to copy the elements of one array to another.  
  
## Syntax  
  
```  
  
      void Copy(  
   const CAtlArray< E, ETraits >& aSrc   
);  
```  
  
#### Parameters  
 `aSrc`  
 The source of the elements to copy to an array.  
  
## Remarks  
 Call this method to overwrite elements of one array with the elements of another array. If necessary, memory will be allocated to accommodate the new elements. It is not possible to copy elements of an array to itself.  
  
 If the existing contents of the array are to be retained, use [CAtlArray::Append](../vs140/CAtlArray--Append.md) instead.  
  
 In debug builds, an ATLASSERT will be raised if the existing `CAtlArray` object is not valid, or if `aSrc` refers to the same object. In release builds, invalid arguments may lead to unpredictable behavior.  
  
> [!NOTE]
>  `CAtlArray::Copy` does not support arrays consisting of elements created with the [CAutoPtr](../vs140/CAutoPtr-Class.md) class.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#5](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#5)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)