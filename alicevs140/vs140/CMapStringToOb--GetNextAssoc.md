---
title: "CMapStringToOb::GetNextAssoc"
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
ms.assetid: e23bd031-6e1a-4a6f-8a32-3e8b34755c8a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::GetNextAssoc
Retrieves the map element at *rNextPosition*, then updates *rNextPosition* to refer to the next element in the map.  
  
## Syntax  
  
```  
  
      void GetNextAssoc(  
   POSITION& rNextPosition,  
   CString& rKey,  
   CObject*& rValue   
) const;  
```  
  
#### Parameters  
 *rNextPosition*  
 Specifies a reference to a **POSITION** value returned by a previous **GetNextAssoc** or **GetStartPosition** call.  
  
 *rKey*  
 Specifies the returned key of the retrieved element (a string).  
  
 *rValue*  
 Specifies the returned value of the retrieved element (a **CObject** pointer). See Remarks for more about this parameter.  
  
## Remarks  
 This function is most useful for iterating through all the elements in the map. Note that the position sequence is not necessarily the same as the key value sequence.  
  
 If the retrieved element is the last in the map, then the new value of *rNextPosition* is set to **NULL**.  
  
 For the *rValue* parameter, be sure to cast your object type to **CObject\*&**, which is what the compiler requires, as shown in the following example:  
  
 [!CODE [NVC_MFCCollections#65](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#65)]  
  
 This is not true of **GetNextAssoc** for maps based on templates.  
  
 The following table shows other member functions that are similar to **CMapStringToOb::GetNextAssoc**.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, void\*&**  *rKey* **, void\*&**  *rValue*  **) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, void\*&**  *rKey* **, WORD&**  *rValue*  **) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, CString&**  *rKey* **, void\*&**  *rValue*  **) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, CString&**  *rKey* **, CString&**  *rValue*  **) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, WORD&**  *rKey* **, CObject\*&**  *rValue*  **) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**void GetNextAssoc( POSITION&**  *rNextPosition* **, WORD&**  *rKey* **, void\*&**  *rValue*  **) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#66](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#66)]  
  
 The results from this program are as follows:  
  
 `Lisa : a CAge at $4724 11`  
  
 `Marge : a CAge at $47A8 35`  
  
 `Homer : a CAge at $4766 36`  
  
 `Bart : a CAge at $45D4 13`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::GetStartPosition](../vs140/CMapStringToOb--GetStartPosition.md)