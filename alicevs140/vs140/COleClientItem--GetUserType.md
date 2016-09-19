---
title: "COleClientItem::GetUserType"
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
ms.assetid: 145c4819-7e00-400f-b382-18d75e2a4c1c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetUserType
Call this function to get the user-visible string describing the OLE item's type, such as "Word document."  
  
## Syntax  
  
```  
  
      void GetUserType(  
   USERCLASSTYPE nUserClassType,  
   CString& rString   
);  
```  
  
#### Parameters  
 *nUserClassType*  
 A value indicating the desired variant of the string describing the OLE item's type. This can have one of the following values:  
  
-   `USERCLASSTYPE_FULL` The full type name displayed to the user.  
  
-   `USERCLASSTYPE_SHORT` A short name (15 characters maximum) for use in pop-up menus and the Edit Links dialog box.  
  
-   `USERCLASSTYPE_APPNAME` Name of the application servicing the class.  
  
 `rString`  
 A reference to a [CString](../vs140/CStringT-Class.md) object to which the string describing the OLE item's type is to be returned.  
  
## Remarks  
 This is often the entry in the system registration database.  
  
 If the full type name is requested but not available, the short name is used instead. If no entry for the type of OLE item is found in the registration database, or if there are no user types registered for the type of OLE item, then the user type currently stored in the OLE item is used. If that user type name is an empty string, "Unknown Object" is used.  
  
 For more information, see [IOleObject::GetUserType](http://msdn.microsoft.com/library/windows/desktop/ms688643) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetType](../vs140/COleClientItem--GetType.md)