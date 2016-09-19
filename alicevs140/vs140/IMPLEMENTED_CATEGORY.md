---
title: "IMPLEMENTED_CATEGORY"
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
ms.assetid: d898ef34-5684-4709-beb9-7114ddd96674
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IMPLEMENTED_CATEGORY
Add an `IMPLEMENTED_CATEGORY` macro to your component's [category map](../vs140/BEGIN_CATEGORY_MAP.md) to specify that it should be registered as implementing the category identified by the `catID` parameter.  
  
## Syntax  
  
```  
  
      IMPLEMENTED_CATEGORY(  
   catID   
)  
```  
  
#### Parameters  
 `catID`  
 [in] A **CATID** constant or variable holding the globally unique identifier (GUID) for the implemented category. The address of `catID` will be taken and added to the map. See the table below for a selection of stock categories.  
  
## Remarks  
 The component categories listed in the map will be registered automatically when the module is registered if the class has an associated [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) or [OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO](../vs140/OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO.md) macro.  
  
 Clients can use the category information registered for the class to determine its capabilities and requirements without having to create an instance of it.  
  
 For more information about component categories, see [What are Component Categories and how do they work?](http://msdn.microsoft.com/library/windows/desktop/ms694322) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### A Selection of Stock Categories  
  
|Description|Symbol|Registry GUID|  
|-----------------|------------|-------------------|  
|Safe For Scripting|CATID_SafeForScripting|{7DD95801-9882-11CF-9FA9-00AA006C42C4}|  
|Safe For Initialization|CATID_SafeForInitializing|{7DD95802-9882-11CF-9FA9-00AA006C42C4}|  
|Simple Frame Site Containment|CATID_SimpleFrameControl|{157083E0-2368-11cf-87B9-00AA006C8166}|  
|Simple Data Binding|CATID_PropertyNotifyControl|{157083E1-2368-11cf-87B9-00AA006C8166}|  
|Advanced Data Binding|CATID_VBDataBound|{157083E2-2368-11cf-87B9-00AA006C8166}|  
|Windowless Controls|CATID_WindowlessObject|{1D06B600-3AE3-11cf-87B9-00AA006C8166}|  
|Internet-Aware Objects|See [Internet Aware Objects](http://msdn.microsoft.com/library/windows/desktop/ms690561) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a sample list.||  
  
## Example  
 [!CODE [NVC_ATL_Windowing#100](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#100)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Category Macros](../vs140/Category-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [BEGIN_CATEGORY_MAP](../vs140/BEGIN_CATEGORY_MAP.md)   
 [REQUIRED_CATEGORY](../vs140/REQUIRED_CATEGORY.md)   
 [END_CATEGORY_MAP](../vs140/END_CATEGORY_MAP.md)