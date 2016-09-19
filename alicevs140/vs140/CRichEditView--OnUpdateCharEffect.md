---
title: "CRichEditView::OnUpdateCharEffect"
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
ms.assetid: a0f45929-ce0e-4a33-9457-836772fac2b3
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnUpdateCharEffect
The framework calls this function to update the command UI for character effect commands.  
  
## Syntax  
  
```  
  
      void OnUpdateCharEffect(  
   CCmdUI* pCmdUI,  
   DWORD dwMask,  
   DWORD dwEffect   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 Pointer to a [CCmdUI](../vs140/CCmdUI-Class.md) object.  
  
 `dwMask`  
 Indicates the character formatting mask.  
  
 `dwEffect`  
 Indicates the character formatting effect.  
  
## Remarks  
 The mask `dwMask` specifies which character formatting attributes to check. The flags `dwEffect` list the character formatting attributes to set/clear.  
  
 For more information on the `dwMask` and `dwEffect` parameters and their potential values, see the corresponding data members of [CHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb787881) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#158](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#158)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)