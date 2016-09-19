---
title: "CComBSTR::LoadString"
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
ms.assetid: 34f81276-8e27-44d4-8c11-81f764b43f2c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::LoadString
Loads a string resource specified by `nID` and stores it in this object.  
  
## Syntax  
  
```  
  
      bool LoadString(  
   HINSTANCE hInst,  
   UINT nID   
) throw();  
bool LoadString(  
   UINT nID   
) throw();  
```  
  
#### Parameters  
 See [LoadString](http://msdn.microsoft.com/library/windows/desktop/ms647486) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **true** if the string is successfully loaded; otherwise, returns **false**.  
  
## Remarks  
 The first function loads the resource from the module identified by you via the `hInst` parameter. The second function loads the resource from the resource module associated with the [CComModule](../vs140/CComModule-Class.md)-derived object used in this project.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#43](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#43)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [ATL and MFC String Conversion Macros](assetId:///6ffb16b0-df9e-4011-a105-f756c3caf3ba)