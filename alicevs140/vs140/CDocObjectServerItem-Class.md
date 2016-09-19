---
title: "CDocObjectServerItem Class"
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
ms.assetid: 530f7156-50c8-4806-9328-602c9133f622
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServerItem Class
Implements OLE server verbs specifically for DocObject servers.  
  
## Syntax  
  
```  
class CDocObjectServerItem : public COleServerItem  
```  
  
## Members  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CDocObjectServerItem::CDocObjectServerItem](#cdocobjectserveritem__cdocobjectserveritem)|Constructs a `CDocObjectServerItem` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CDocObjectServerItem::GetDocument](#cdocobjectserveritem__getdocument)|Retrieves a pointer to the document that contains the item.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CDocObjectServerItem::OnHide](#cdocobjectserveritem__onhide)|Throws an exception if the framework tries to hide a DocObject item.|  
|[CDocObjectServerItem::OnShow](#cdocobjectserveritem__onshow)|Called by the framework to make the DocObject item in-place active. If the item is not a DocObject, calls [COleServerItem::OnShow](../vs140/COleServerItem-Class.md#coleserveritem__onshow).|  
  
## Remarks  
 `CDocObjectServerItem` defines overridable member functions: [OnHide](#cdocobjectserveritem__onhide), [OnOpen](assetId:///7a9b1363-6ad8-4732-9959-4e35c07644fd), and [OnShow](#cdocobjectserveritem__onshow).  
  
 To use `CDocObjectServerItem`, assure that the [OnGetEmbeddedItem](../vs140/COleServerDoc-Class.md#coleserverdoc__ongetembeddeditem) override in your `COleServerDoc`-derived class returns a new `CDocObjectServerItem` object. If you need to change any functionality in your item, you can create a new instance of your own `CDocObjectServerItem`-derived class.  
  
 For further information on DocObjects, see [CDocObjectServer](../vs140/CDocObjectServer-Class.md) and [COleCmdUI](../vs140/COleCmdUI-Class.md) in the                 *MFC Reference*. Also see [Internet First Steps: Active Documents](../vs140/Active-Documents-on-the-Internet.md) and [Active Documents](../vs140/Active-Documents-on-the-Internet.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CDocItem](../vs140/CDocItem-Class.md)  
  
 [COleServerItem](../vs140/COleServerItem-Class.md)  
  
 `CDocObjectServerItem`  
  
## Requirements  
 **Header:** afxdocob.h  
  
##  <a name="cdocobjectserveritem__cdocobjectserveritem"></a>  CDocObjectServerItem::CDocObjectServerItem  
 Constructs a `CDocObjectServerItem` object.  
  
```  
CDocObjectServerItem(    COleServerDoc* pServerDoc, BOOL bAutoDelete );  
  
```  
  
### Parameters  
 `pServerDoc`  
 A pointer to the document that will contain the new DocObject item.  
  
 `bAutoDelete`  
 Indicates whether the object can be deleted when a link to it is released. Set the argument to **FALSE** if the `CDocObjectServerItem` object is an integral part of your document's data. Set it to **TRUE** if the object is a secondary structure used to identify a range in your document's data that can be deleted by the framework.  
  
##  <a name="cdocobjectserveritem__getdocument"></a>  CDocObjectServerItem::GetDocument  
 Retrieves a pointer to the document that contains the item.  
  
```  
COleServerDoc* GetDocument( ) const;  
  
```  
  
### Return Value  
 A pointer to the document that contains the item; **NULL** if the item is not part of a document.  
  
### Remarks  
 This allows access to the server document that you passed as an argument to the [CDocObjectServerItem](#cdocobjectserveritem__cdocobjectserveritem) constructor.  
  
##  <a name="cdocobjectserveritem__onhide"></a>  CDocObjectServerItem::OnHide  
 Called by the framework to hide the item.  
  
```  
virtual void OnHide( );  
  
```  
  
### Remarks  
 The default implementation throws an exception if the item is a DocObject. You cannot hide an active DocObject item because it takes the whole view. You must deactivate the DocObject item to make it disappear. If the item is not a DocObject, the default implementation calls [COleServerItem::OnHide](../vs140/COleServerItem-Class.md#coleserveritem__onhide).  
  
##  <a name="cdocobjectserveritem__onshow"></a>  CDocObjectServerItem::OnShow  
 Called by the framework to instruct the server application to make the DocObject item in-place active.  
  
```  
virtual void OnShow( );  
  
```  
  
### Remarks  
 If the item is not a DocObject, the default implementation calls [COleServerItem::OnShow](../vs140/COleServerItem-Class.md#coleserveritem__onopen). Override this function if you want to perform special processing when opening a DocObject item.  
  
## See Also  
 [Base Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer](../vs140/CDocObjectServer-Class.md)   
 [COleDocObjectItem](../vs140/COleDocObjectItem-Class.md)