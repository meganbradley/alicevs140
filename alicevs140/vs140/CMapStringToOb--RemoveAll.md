---
title: "CMapStringToOb::RemoveAll"
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
ms.assetid: 23a8d68e-b35e-4228-8a34-bfc5e8611202
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::RemoveAll
Removes all the elements from this map and destroys the `CString` key objects.  
  
## Syntax  
  
```  
  
void RemoveAll( );  
```  
  
## Remarks  
 The `CObject` objects referenced by each key are not destroyed. The `RemoveAll` function can cause memory leaks if you do not ensure that the referenced `CObject` objects are destroyed.  
  
 The function works correctly if the map is already empty.  
  
 The following table shows other member functions that are similar to `CMapStringToOb::RemoveAll`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**void RemoveAll( );**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**void RemoveAll( );**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**void RemoveAll( );**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**void RemoveAll( );**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**void RemoveAll( );**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**void RemoveAll( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#69)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::RemoveKey](../vs140/CMapStringToOb--RemoveKey.md)