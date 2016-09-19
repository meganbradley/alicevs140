---
title: "CMenuTearOffManager Class"
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
ms.assetid: ab7ca272-ce42-4678-95f7-6ad75038f5a0
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenuTearOffManager Class
Manages tear-off menus. A tear-off menu is a menu on the menu bar. The user can remove a tear-off menu from the menu bar, causing the tear-off menu to float.  
  
## Syntax  
  
```  
class CMenuTearOffManager : public CObject  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMenuTearOffManager::CMenuTearOffManager](#cmenutearoffmanager__cmenutearoffmanager)|Constructs a `CMenuTearOffManager` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMenuTearOffManager::Build](#cmenutearoffmanager__build)||  
|[CMenuTearOffManager::GetRegPath](#cmenutearoffmanager__getregpath)||  
|[CMenuTearOffManager::Initialize](#cmenutearoffmanager__initialize)|Initializes a `CMenuTearOffManager` object.|  
|[CMenuTearOffManager::IsDynamicID](#cmenutearoffmanager__isdynamicid)||  
|[CMenuTearOffManager::Parse](#cmenutearoffmanager__parse)||  
|[CMenuTearOffManager::Reset](#cmenutearoffmanager__reset)||  
|[CMenuTearOffManager::SetInUse](#cmenutearoffmanager__setinuse)||  
|[CMenuTearOffManager::SetupTearOffMenus](#cmenutearoffmanager__setuptearoffmenus)||  
  
## Remarks  
 In order to use tear-off menus in your application, you must have a `CMenuTearOffManager` object. In most cases, you won't create or initialize a `CMenuTearOffManager` object directly. This is handled for you when you call the [CWinAppEx::EnableTearOffMenus](../vs140/CWinAppEx-Class.md#cwinappex__enabletearoffmenus) function.  
  
## Example  
 The following example demonstrates how to construct and initialize a `CMenuTearOffManager` object by calling the `CWinAppEX::EnableTearOffMenus` method. This code snippet is part of the [Word Pad sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_WordPad#12](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_WordPad#12)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMenuTearOffManager](../vs140/CMenuTearOffManager-Class.md)  
  
## Requirements  
 **Header:** afxmenutearoffmanager.h  
  
##  <a name="cmenutearoffmanager__build"></a>  CMenuTearOffManager::Build  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void Build(  
   UINT uiTearOffBarID,  
   CString& strText  
);  
```  
  
### Parameters  
 [in] `uiTearOffBarID`  
  [in] `strText`  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__cmenutearoffmanager"></a>  CMenuTearOffManager::CMenuTearOffManager  
 Constructs a [CMenuTearOffManager](../vs140/CMenuTearOffManager-Class.md) object.  
  
```  
CMenuTearOffManager();  
```  
  
### Remarks  
 In most cases, you should not create a `CMenuTearOffManager` manually. The framework of your application creates the `CMenuTearOffManager` object when you call [CWinAppEx::EnableTearOffMenus](../vs140/CWinAppEx-Class.md#cwinappex__enabletearoffmenus).  
  
##  <a name="cmenutearoffmanager__getregpath"></a>  CMenuTearOffManager::GetRegPath  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
LPCTSTR GetRegPath() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__initialize"></a>  CMenuTearOffManager::Initialize  
 Initializes a [CMenuTearOffManager](../vs140/CMenuTearOffManager-Class.md) object.  
  
```  
BOOL Initialize(  
   LPCTSTR lpszRegEntry,  
   UINT uiTearOffMenuFirst,  
   UINT uiTearOffMenuLast  
);  
```  
  
### Parameters  
 [in] `lpszRegEntry`  
 A string that contains the path of a registry entry. Your applications stores the settings for tear-off bars in this registry entry.  
  
 [in] `uiTearOffMenuFirst`  
 The first menu ID for a tear-off menu.  
  
 [in] `uiTearOffMenuLast`  
 The last menu ID for a tear-off menu.  
  
### Return Value  
 Nonzero if successful; otherwise 0.  
  
### Remarks  
 The range of menu IDs from `uiTearOffMenuFirst` to `uiTearOffMenuLast` must be a continuous interval. The interval defines the number of tear-off menus that can appear at the same time in the application.  
  
##  <a name="cmenutearoffmanager__isdynamicid"></a>  CMenuTearOffManager::IsDynamicID  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
BOOL IsDynamicID(  
   UINT uiID  
) const;  
```  
  
### Parameters  
 [in] `uiID`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__parse"></a>  CMenuTearOffManager::Parse  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
UINT Parse(  
   CString& str  
);  
```  
  
### Parameters  
 [in] `str`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__reset"></a>  CMenuTearOffManager::Reset  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void Reset(  
   HMENU hmenu  
);  
```  
  
### Parameters  
 [in] `hmenu`  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__setinuse"></a>  CMenuTearOffManager::SetInUse  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void SetInUse(  
   UINT uiCmdId,  
   BOOL bUse = TRUE  
);  
```  
  
### Parameters  
 [in] `uiCmdId`  
  [in] `bUse`  
  
### Remarks  
  
##  <a name="cmenutearoffmanager__setuptearoffmenus"></a>  CMenuTearOffManager::SetupTearOffMenus  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void SetupTearOffMenus(  
   HMENU hMenu  
);  
```  
  
### Parameters  
 [in] `hMenu`  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)