---
title: __ll_rshift |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __ll_rshift_cpp
- __ll_rshift
dev_langs:
- C++
helpviewer_keywords:
- __ll_rshift intrinsic
- ll_rshift intrinsic
ms.assetid: ef13b732-d122-44a0-add9-f5544a2c4ab2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8df70d0ba5c0f957620ee204256b6c92ce4c01f1
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45722067"
---
# <a name="llrshift"></a>__ll_rshift
**Microsoft 专用**  
  
 第二个参数指定的位数右移由右侧的第一个参数指定的 64 位值。  
  
## <a name="syntax"></a>语法  
  
```  
__int64 __ll_rshift(  
   __int64 Mask,  
   int nBit  
);  
```  
  
#### <a name="parameters"></a>参数  
*掩码*<br/>
[in]要右移位的 64 位整数值。  
  
*nBit*<br/>
[in]要切换，请取模 64 在 x64 上，并取模运算在 x86 上的 32 位的数。  
  
## <a name="return-value"></a>返回值  
 掩码移动`nBit`位。  
  
## <a name="requirements"></a>要求  
  
|内部函数|体系结构|  
|---------------|------------------|  
|`__ll_rshift`|x86、x64|  
  
 **标头文件** \<intrin.h >  
  
## <a name="remarks"></a>备注  
 如果第二个参数是否大于 64 在 x64 (32 x86 上) 上，该数字执行取模 64 (在 x86 上为 32) 若要确定移动的位数编号。 `ll`前缀指示这是一个操作上`long long`，另一个名称为`__int64`，64 位有符号整数类型。  
  
## <a name="example"></a>示例  
  
```  
// ll_rshift.cpp  
// compile with: /EHsc  
// processor: x86, x64  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(__ll_rshift)  
  
int main()  
{  
   __int64 Mask = - 0x100;  
   int nBit = 4;  
   cout << hex << Mask << endl;  
   cout << " - " << (- Mask) << endl;  
   Mask = __ll_rshift(Mask, nBit);  
   cout << hex << Mask << endl;  
   cout << " - " << (- Mask) << endl;  
}  
```  
  
## <a name="output"></a>输出  
  
```  
ffffffffffffff00  
 - 100  
fffffffffffffff0  
 - 10  
```  
  
 **请注意**如果`_ull_rshift`已被使用，向右移动值的 MSB 的是零，因此所需的结果将不在负值的情况下获取。  
  
**结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [编译器内部函数](../intrinsics/compiler-intrinsics.md)   
 [__ll_lshift](../intrinsics/ll-lshift.md)   
 [__ull_rshift](../intrinsics/ull-rshift.md)