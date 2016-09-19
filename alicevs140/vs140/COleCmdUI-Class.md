---
title: "COleCmdUI Class"
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
ms.assetid: a2d5ce08-6657-45d3-8673-2a9f32d50eec
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCmdUI Class
Implements a method for MFC to update the state of user-interface objects related to the `IOleCommandTarget`-driven features of your application.  
  
## Syntax  
  
```  
class COleCmdUI : public CCmdUI  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[COleCmdUI::COleCmdUI](#colecmdui__colecmdui)|Constructs a `COleCmdUI` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[COleCmdUI::Enable](#colecmdui__enable)|Sets or clears the enable command flag.|  
|[COleCmdUI::SetCheck](#colecmdui__setcheck)|Sets the state of an on/off toggle command.|  
|[COleCmdUI::SetText](#colecmdui__settext)|Returns a text name or status string for a command.|  
  
## Remarks  
 In an application that is not enabled for DocObjects, when the user views a menu in the application, MFC processes **UPDATE_COMMAND_UI** notifcations. Each notification is given a [CCmdUI](../vs140/CCmdUI-Class.md) object that can be manipulated to reflect the state of a particular command. However, when your application is enabled for DocObjects, MFC processes **UPDATE_OLE_COMMAND_UI** notifications and assigns `COleCmdUI` objects.  
  
 `COleCmdUI` allows a DocObject to receive commands that originate in its container's user interface (such as FileNew, Open, Print, and so on), and allows a container to receive commands that originate in the DocObject's user interface. Although `IDispatch` could be used to dispatch the same commands, `IOleCommandTarget` provides a simpler way to query and execute because it relies on a standard set of commands, usually without arguments, and no type information is involved. `COleCmdUI` can be used to enable, update, and set other properties of DocObject user interface commands. When you want to invoke the command, call [COleServerDoc::OnExecOleCmd](../vs140/COleServerDoc-Class.md#coleserverdoc__onexecolecmd).  
  
 For further information on DocObjects, see [CDocObjectServer](../vs140/CDocObjectServer-Class.md) and [CDocObjectServerItem](../vs140/CDocObjectServerItem-Class.md). Also see [Internet First Steps: Active Documents](../vs140/Active-Documents-on-the-Internet.md) and [Active Documents](../vs140/Active-Documents-on-the-Internet.md).  
  
## Inheritance Hierarchy  
 [CCmdUI](../vs140/CCmdUI-Class.md)  
  
 `COleCmdUI`  
  
## Requirements  
 **Header:** afxdocobj.h  
  
##  <a name="colecmdui__colecmdui"></a>  COleCmdUI::COleCmdUI  
 Constructs a `COleCmdUI` object associated with a particular user-interface command.  
  
```  
COleCmdUI(    OLECMD*  rgCmds ,    ULONG  cCmds ,    const GUID*  m_pGroup );  
  
```  
  
### Parameters  
 `rgCmds`  
 A list of supported commands associated with the given GUID. The **OLECMD** structure associates commands with command flags.  
  
 *cCmds*  
 The count of commands in `rgCmds`.  
  
 `pGroup`  
 A pointer to a GUID that identifies a set of commands.  
  
### Remarks  
 The `COleCmdUI` object provides a programmatic interface for updating DocObject user-interface objects such as menu items or control-bar buttons. The user-interface objects can be enabled, disabled, checked, and/or cleared through the `COleCmdUI` object.  
  
##  <a name="colecmdui__enable"></a>  COleCmdUI::Enable  
 Call this function to set the command flag of the `COleCmdUI` object to **OLECOMDF_ENABLED**, which tells the interface the command is available and enabled, or to clear the command flag.  
  
```  
virtual void Enable(    BOOL  bOn );  
  
```  
  
### Parameters  
 `bOn`  
 Indicates whether the command associated with the `COleCmdUI` object should be enabled or disabled. Nonzero enables the command; 0 disables the command.  
  
##  <a name="colecmdui__setcheck"></a>  COleCmdUI::SetCheck  
 Call this function to set the state of an on/off toggle command.  
  
```  
virtual void SetCheck(    int  nCheck );  
  
```  
  
### Parameters  
 `nCheck`  
 A value determining the state to set an on/off toggle command. Values are:  
  
|Value|Description|  
|-----------|-----------------|  
|**1**|Sets the command to on.|  
|**2**|Sets the command to indeterminate; the state cannot be determined because the attribute of this command is in both on and off states in the relevant selection.|  
|any other value|Sets the command to off.|  
  
##  <a name="colecmdui__settext"></a>  COleCmdUI::SetText  
 Call this function to return a text name or status string for a command.  
  
```  
virtual void SetText(    LPCTSTR lpszText );  
  
```  
  
### Parameters  
 `lpszText`  
 A pointer to the text to be used with the command.  
  
## See Also  
 [Base Class](../vs140/CCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)