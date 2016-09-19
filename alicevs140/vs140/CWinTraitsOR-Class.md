---
title: "CWinTraitsOR Class"
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
ms.assetid: 1eb7b1e8-a9bd-411b-a30a-35a8a10af989
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinTraitsOR Class
This class provides a method for standardizing the styles used when creating a window object.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template <  
   DWORD  t_dwStyle  
   = 0,  
   DWORD t_dwExStyle  
   = 0,  
   class TWinTraits = CControlWinTraits >  
   class CWinTraitsOR  
  
```  
  
#### Parameters  
 `t_dwStyle`  
 Default window styles.  
  
 `t_dwExStyle`  
 Default extended window styles.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CWinTraitsOR::GetWndExStyle](../vs140/CWinTraitsOR--GetWndExStyle.md)|Retrieves the extended styles for the `CWinTraitsOR` object.|  
|[CWinTraitsOR::GetWndStyle](../vs140/CWinTraitsOR--GetWndStyle.md)|Retrieves the standard styles for the `CWinTraitsOR` object.|  
  
## Remarks  
 This [window traits](../vs140/Understanding-Window-Traits.md) class provides a simple method for standardizing the styles used for the creation of an ATL window object. Use a specialization of this class as a template parameter to [CWindowImpl](../vs140/CWindowImpl-Class.md) or another of ATL's window classes to specify the minimum set of standard and extended styles to be used for instances of that window class.  
  
 Use a specialization of this template if you want to ensure that certain styles are set for all instances of the window class while permitting other styles to be set on a per-instance basis in the call to [CWindowImpl::Create](../vs140/CWindowImpl--Create.md).  
  
 If you want to provide default window styles that will be used only when no other styles are specified in the call to `CWindowImpl::Create`, use [CWinTraits](../vs140/CWinTraits-Class.md) instead.  
  
## Requirements  
 **Header:** atlwin.h  
  
##  <a name="cwintraitsor__getwndstyle"></a>  CWinTraitsOR::GetWndStyle  
 Call this function to retrieve a combination (using the logical OR operator) of the standard styles of the `CWinTraits` object and the default styles specified by `t_dwStyle`.  
  
```  
  
static DWORD GetWndStyle(  
      DWORD  dwStyle  
   );  
  
```  
  
### Parameters  
 `dwStyle`  
 Styles used for creation of a window.  
  
### Return Value  
 A combination of styles that are passed in `dwStyle` and the default ones specified by `t_dwStyle`, using the logical OR operator.  
  
##  <a name="cwintraitsor__getwndexstyle"></a>  CWinTraitsOR::GetWndExStyle  
 Call this function to retrieve a combination (using the logical OR operator) of the extended styles of the `CWinTraits` object and the default styles specified by `t_dwStyle`.  
  
```  
  
static DWORD GetWndExStyle(  
      DWORD  dwExStyle  
   );  
  
```  
  
### Parameters  
 `dwExStyle`  
 Extended styles used for creation of a window.  
  
### Return Value  
 A combination of extended styles that are passed in `dwExStyle` and default ones specified by `t_dwExStyle`, using the logical OR operator  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Understanding Window Traits](../vs140/Understanding-Window-Traits.md)