---
title: "CMapStringToOb::operator"
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
ms.assetid: a1e694d3-c5ce-4ff2-a750-a6040e8c758f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::operator
A convenient substitute for the `SetAt` member function.  
  
## Syntax  
  
```  
  
      CObject*& operator [ ](LPCTSTR key);  
```  
  
## Return Value  
 A reference to a pointer to a `CObject` object; or **NULL** if the map is empty or `key` is out of range.  
  
## Remarks  
 Thus it can be used only on the left side of an assignment statement (an l-value). If there is no map element with the specified key, then a new element is created.  
  
 There is no "right side" (r-value) equivalent to this operator because there is a possibility that a key may not be found in the map. Use the `Lookup` member function for element retrieval.  
  
 The following table shows other member functions that are similar to **CMapStringToOb::operator []**.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**void\*& operator[](void\***  `key`  **\);**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**WORD& operator[](void\***  `key`  **\);**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**void\*& operator[](LPCTSTR**  `key`  **\);**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**CString& operator[](LPCTSTR**  `key`  **\);**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**CObject\*& operator[](WORD**  `key`  **\);**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**void\*& operator[](WORD**  `key`  **\);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#72](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#72)]  
  
 The results from this program are as follows:  
  
 `Operator [] example: A CMapStringToOb with 2 elements`  
  
 `[Lisa] = a CAge at $4A02 11`  
  
 `[Bart] = a CAge at $497E 13`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::SetAt](../vs140/CMapStringToOb--SetAt.md)   
 [CMapStringToOb::Lookup](../vs140/CMapStringToOb--Lookup.md)