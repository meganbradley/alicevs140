---
title: "CBitmapButton::LoadBitmaps"
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
ms.assetid: 627bf611-ff85-4e16-812f-69cd5a9038f8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmapButton::LoadBitmaps
Use this function when you want to load bitmap images identified by their resource names or ID numbers, or when you cannot use the `AutoLoad` function because, for example, you are creating a bitmap button that is not part of a dialog box.  
  
## Syntax  
  
```  
  
      BOOL LoadBitmaps(  
   LPCTSTR lpszBitmapResource,  
   LPCTSTR lpszBitmapResourceSel = NULL,  
   LPCTSTR lpszBitmapResourceFocus = NULL,  
   LPCTSTR lpszBitmapResourceDisabled = NULL   
);  
BOOL LoadBitmaps(  
   UINT nIDBitmapResource,  
   UINT nIDBitmapResourceSel = 0,  
   UINT nIDBitmapResourceFocus = 0,  
   UINT nIDBitmapResourceDisabled = 0   
);  
```  
  
#### Parameters  
 *lpszBitmapResource*  
 Points to the null-terminated string that contains the name of the bitmap for a bitmap button's normal or "up" state. Required.  
  
 *lpszBitmapResourceSel*  
 Points to the null-terminated string that contains the name of the bitmap for a bitmap button's selected or "down" state. May be **NULL**.  
  
 *lpszBitmapResourceFocus*  
 Points to the null-terminated string that contains the name of the bitmap for a bitmap button's focused state. May be **NULL**.  
  
 *lpszBitmapResourceDisabled*  
 Points to the null-terminated string that contains the name of the bitmap for a bitmap button's disabled state. May be **NULL**.  
  
 *nIDBitmapResource*  
 Specifies the resource ID number of the bitmap resource for a bitmap button's normal or "up" state. Required.  
  
 *nIDBitmapResourceSel*  
 Specifies the resource ID number of the bitmap resource for a bitmap button's selected or "down" state. May be 0.  
  
 *nIDBitmapResourceFocus*  
 Specifies the resource ID number of the bitmap resource for a bitmap button's focused state. May be 0.  
  
 *nIDBitmapResourceDisabled*  
 Specifies the resource ID number of the bitmap resource for a bitmap button's disabled state. May be 0.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#58](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#58)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CBitmapButton Class](../vs140/CBitmapButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBitmapButton::AutoLoad](../vs140/CBitmapButton--AutoLoad.md)   
 [CBitmapButton::SizeToContent](../vs140/CBitmapButton--SizeToContent.md)   
 [CButton::Create](../vs140/CButton--Create.md)   
 [CBitmap::LoadBitmap](../vs140/CBitmap--LoadBitmap.md)