---
title: "CLinkCtrl::Create"
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
ms.assetid: 156ec0f3-bdd7-4198-92da-194f0fc5a6cc
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::Create
Creates a link control and attaches it to a `CLinkCtrl` object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   LPCTSTR lpszLinkMarkup,   
   DWORD dwStyle,   
   const RECT& rect,   
   CWnd* pParentWnd,   
   UINT nID  
);  
virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `lpszLinkMarkup`  
 Pointer to a zero-terminated string that contains the marked up text to display. For more information, see the section "Markup and Link Access" in the topic [Overview of SysLink Controls](http://msdn.microsoft.com/library/windows/desktop/bb760706) in the [MSDN Library](http://go.microsoft.com/fwlink/?linkid=556).  
  
 `dwStyle`  
 Specifies the link control's style. Apply any combination of control styles. See [Common Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775498) in the `Windows SDK` for more information.  
  
 `rect`  
 Specifies the link control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the link control's parent window. It must not be `NULL`.  
  
 `nID`  
 Specifies the link control's ID.  
  
## Return Value  
 `true` if initialization was successful; otherwise `false`.  
  
## Remarks  
 You construct a `CLinkCtrl` object in two steps. First, call the constructor and then call `Create`, which creates the link control and attaches it to the `CLinkCtrl` object. If you want to use extended windows styles with your control, call [CLinkCtrl::CreateEx](../vs140/CLinkCtrl--CreateEx.md) instead of `Create`.  
  
 The second form of the `Create` method is deprecated. Use the first form that specifies the `lpszLinkMarkup` parameter.  
  
## Example  
 The following code example defines two variables, named `m_Link1` and `m_Link2`, that are used to access two link controls.  
  
 [!CODE [NVC_MFC_CLinkCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CLinkCtrl_s1#2)]  
  
## Example  
 The following code example creates one link control based on the location of another link control. The resource loader creates the first link control when your application starts. When your application enters the OnInitDialog method, you create the second link control relative to the position of the first link control. Then you resize the second link control to fit the text that it displays.  
  
 [!CODE [NVC_MFC_CLinkCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CLinkCtrl_s1#1)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::CreateEx](../vs140/CLinkCtrl--CreateEx.md)