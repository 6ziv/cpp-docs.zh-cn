---
title: _bittest、_bittest64 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _bittest64
- _bittest_cpp
- _bittest64_cpp
- _bittest
dev_langs:
- C++
helpviewer_keywords:
- _bittest intrinsic
- _bittest64 intrinsic
- bt instruction
ms.assetid: 15e62afb-abea-4ee7-a6b1-13efa2034937
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d6d316c272a2db1bdb3351aa54f72db46dd66583
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713201"
---
# <a name="bittest-bittest64"></a>_bittest、_bittest64
**Microsoft 专用**  
  
生成 `bt` 指令，从而检查地址 `b` 的位置 `a` 中的位，并返回该位的值。  
  
## <a name="syntax"></a>语法  
  
```  
unsigned char _bittest(  
   long const *a,  
   long b  
);  
unsigned char _bittest64(  
   __int64 const *a,  
   __int64 b  
);  
```  
  
### <a name="parameters"></a>参数  
*a*<br/>
[in]指向要检查的内存的指针。  
  
*b*<br/>
[in]要测试的位位置。  
  
### <a name="return-value"></a>返回值  
指定位置的位。  
  
## <a name="requirements"></a>要求  
  
|内部函数|体系结构|Header|  
|---------------|------------------|------------|  
|`_bittest`|x86、 ARM、 x64|\<intrin.h>|  
|`_bittest64`|ARM、 x64|\<intrin.h>|  
  
## <a name="remarks"></a>备注  
此例程仅可用作内部函数。  
  
## <a name="example"></a>示例  
  
```cpp  
// bittest.cpp  
// processor: x86, ARM, x64  
  
#include <stdio.h>  
#include <intrin.h>  
  
long num = 78002;  
  
int main()  
{  
    unsigned char bits[32];  
    long nBit;  
  
    printf_s("Number: %d\n", num);  
  
    for (nBit = 0; nBit < 31; nBit++)  
    {  
        bits[nBit] = _bittest(&num, nBit);  
    }  
  
    printf_s("Binary representation:\n");  
    while (nBit--)  
    {  
        if (bits[nBit])  
            printf_s("1");  
        else  
            printf_s("0");  
    }  
}  
```  
  
```Output  
Number: 78002  
Binary representation:  
0000000000000010011000010110010  
```  
  
**结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
[编译器内部函数](../intrinsics/compiler-intrinsics.md)