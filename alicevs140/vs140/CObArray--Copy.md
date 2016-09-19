---
title: "CObArray::Copy"
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
ms.assetid: 6e0f3e2e-2c36-464b-a8a3-4dc28442ae4d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::Copy
Call this member function to overwrite the elements of the given array with the elements of another array of the same type.  
  
## Syntax  
  
```  
  
      void Copy(  
   const CObArray& src   
);  
```  
  
#### Parameters  
 *src*  
 Source of the elements to be copied to the array.  
  
## Remarks  
 **Copy** does not free memory; however, if necessary, **Copy** may allocate extra memory to accommodate the elements copied to the array.  
  
 The following table shows other member functions that are similar to `CObArray::Copy`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**void Copy( const CByteArray&**  *src*  **);**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**void Copy( const CDWordArray&**  *src*  **);**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void Copy( const CPtrArray&**  *src*  **);**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**void Copy( const CStringArray&**  *src*  **);**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**void Copy( const CUIntArray&**  *src*  **);**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**void Copy( const CWordArray&**  *src*  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#77](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#77)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::Append](../vs140/CObArray--Append.md)