---
title: "CObArray::GetData"
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
ms.assetid: e80ce27a-8ab9-45e6-a151-f108039e4573
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::GetData
Use this member function to gain direct access to the elements in the array.  
  
## Syntax  
  
```  
  
      const CObject** GetData( ) const;    
CObject** GetData( );  
```  
  
## Return Value  
 A pointer to the array of `CObject` pointers.  
  
## Remarks  
 If no elements are available, `GetData` returns a null value.  
  
 While direct access to the elements of an array can help you work more quickly, use caution when calling `GetData`; any errors you make directly affect the elements of your array.  
  
 The following table shows other member functions that are similar to `CObArray::GetData`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**const BYTE\* GetData( ) const;BYTE\* GetData( );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**const DWORD\* GetData( ) const;DWORD\* GetData( );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**const void\*\* GetData( ) const;void\*\* GetData( );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**const CString\* GetData( ) const;CString\* GetData( );**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**const UINT\* GetData( ) const;UINT\* GetData( );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**const WORD\* GetData( ) const;WORD\* GetData( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#81](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#81)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetAt](../vs140/CObArray--GetAt.md)   
 [CObArray::SetAt](../vs140/CObArray--SetAt.md)   
 [CObArray::ElementAt](../vs140/CObArray--ElementAt.md)