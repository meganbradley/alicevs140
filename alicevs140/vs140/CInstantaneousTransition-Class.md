---
title: "CInstantaneousTransition Class"
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
ms.assetid: c3d5121f-2c6b-4221-9e57-10e082a31120
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInstantaneousTransition Class
Encapsulates an instantaneous transition.  
  
## Syntax  
  
```  
class CInstantaneousTransition : public CBaseTransition;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CInstantaneousTransition::CInstantaneousTransition](#cinstantaneoustransition__cinstantaneoustransition)|Constructs a transition object and initializes its final value.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CInstantaneousTransition::Create](#cinstantaneoustransition__create)|Calls the transition library to create encapsulated transition COM object. (Overrides [CBaseTransition::Create](../vs140/CBaseTransition-Class.md#cbasetransition__create).)|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CInstantaneousTransition::m_dblFinalValue](#cinstantaneoustransition__m_dblfinalvalue)|The value of the animation variable at the end of the transition.|  
  
## Remarks  
 During an instantaneous transition, the value of the animation variable changes instantly from its current value to a specified final value. The duration of this transition is always zero. Because all transitions are cleared automatically, it's recommended to allocated them using operator new. The encapsulated IUIAnimationTransition COM object is created by CAnimationController::AnimateGroup, until then it's NULL. Changing member variables after creation of this COM object has no effect.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CBaseTransition](../vs140/CBaseTransition-Class.md)  
  
 [CInstantaneousTransition](../vs140/CInstantaneousTransition-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="cinstantaneoustransition__cinstantaneoustransition"></a>  CInstantaneousTransition::CInstantaneousTransition  
 Constructs a transition object and initializes its final value.  
  
```  
CInstantaneousTransition(  
   DOUBLE dblFinalValue  
);  
```  
  
### Parameters  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
##  <a name="cinstantaneoustransition__create"></a>  CInstantaneousTransition::Create  
 Calls the transition library to create encapsulated transition COM object.  
  
```  
virtual BOOL Create(  
   IUIAnimationTransitionLibrary* pLibrary,  
   IUIAnimationTransitionFactory* */  
);  
```  
  
### Parameters  
 `pLibrary`  
 A pointer to transition library, which is responsible for creation of standard transitions.  
  
### Return Value  
 TRUE if transition is created successfully; otherwise FALSE.  
  
##  <a name="cinstantaneoustransition__m_dblfinalvalue"></a>  CInstantaneousTransition::m_dblFinalValue  
 The value of the animation variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalValue;  
```  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)