---
title: strtoumax、_strtoumax_l、wcstoumax、_wcstoumax_l | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _wcstoumax_l
- _strtoumax_l
- wcstoumax
- strtoumax
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-convert-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- wcstoumax
- _tcstoumax
- _strtoumax_l
- _wcstoumax_l
- _tcstoumax_l
- strtoumax
dev_langs:
- C++
helpviewer_keywords:
- _strtoumax_l function
- conversion functions
- wcstoumax function
- _wcstoumax_l function
- strtoumax function
ms.assetid: 566769f9-495b-4508-b9c6-02217a578897
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0691e26387f70e80718d8af84ba9ff18ad7fd489
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
ms.locfileid: "32417799"
---
# <a name="strtoumax-strtoumaxl-wcstoumax-wcstoumaxl"></a>strtoumax、_strtoumax_l、wcstoumax、_wcstoumax_l

将字符串转换为受支持的最大无符号整数类型的整数值。

## <a name="syntax"></a>语法

```C
uintmax_t strtoumax(
   const char *strSource,
   char **endptr,
   int base
);
uintmax_t _strtoumax_l(
   const char *strSource,
   char **endptr,
   int base,
   _locale_t locale
);
uintmax_t wcstoumax(
   const wchar_t *strSource,
   wchar_t **endptr,
   int base
);
uintmax_t _wcstoumax_l(
   const wchar_t *strSource,
   wchar_t **endptr,
   int base,
   _locale_t locale
);
```

### <a name="parameters"></a>参数

*strSource*<br/>
要转换的 null 终止的字符串。

*endptr*<br/>
指向停止扫描的字符的指针。

*base*<br/>
要使用的基数。

*locale*<br/>
要使用的区域设置。

## <a name="return-value"></a>返回值

**strtoumax**返回转换后的值，如果有，或**UINTMAX_MAX**上溢出。 **strtoumax**如果可以不执行任何转换，则返回 0。 **wcstoumax**类似地为返回值**strtoumax**。 对于这两个函数， **errno**设置为**ERANGE**如果发生溢出或下溢。

有关返回代码的详细信息，请参阅 [errno、_doserrno、_sys_errlist 和 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)。

## <a name="remarks"></a>备注

其中每个函数将转换输入的字符串*strSource*到**uintmax_t**整数值。

**strtoumax**停止读取字符串*strSource*不能将其识别为一个数字部分的第一个字符。 这可能是终止 null 字符，也可能是大于或等于的第一个数字字符*基*。 **LC_NUMERIC**类别设置的区域设置确定基数字符在识别*strSource*。 有关详细信息，请参阅 [setlocale、_wsetlocale](setlocale-wsetlocale.md)。 **strtoumax**和**wcstoumax**使用当前区域设置;**_strtoumax_l**和 **_wcstoumax_l**是相同，只不过它们改用传入的区域设置。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。

如果*endptr*不**NULL**，停止扫描的字符的指针指向的位置存储*endptr*。 如果可以不执行任何转换 （未找到有效的数字或指定了无效的基本） 的值*strSource*指向的位置存储*endptr*。

宽字符版本**strtoumax**是**wcstoumax**; 其*strSource*参数是宽字符字符串。 否则，这些函数具有相同行为。

### <a name="generic-text-routine-mappings"></a>一般文本例程映射

|TCHAR.H 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_tcstoumax**|**strtoumax**|**strtoumax**|**wcstoumax**|
|**_tcstoumax_l**|**strtoumax_l**|**_strtoumax_l**|**_wcstoumax_l**|

**strtoumax**需要*strSource*以指向以下形式的字符串：

> [*空白*] [{**+** &#124; **-**}] [**0** [{ **x**&#124; **X** }]] [*数字*&#124; *字母*]  

A*空白*可能包含空格和制表符字符，将被忽略。 *数字*是一个或多个十进制数字。 *字母*中的一个或多个字母 a 到 z （或 A 至 Z）。 不符合此形式的第一个字符停止扫描。 如果*基*为介于 2 和 36，之间，则它可作为数字的基数。 如果*基*为 0，所指向的字符串的初始字符*strSource*用于确定基。 如果第一个字符为“0”，且第二个字符不为“x”或“X”，则将该字符串视为八进制整数。 如果第一个字符为“0”，且第二个字符为“x”或“X”，则将该字符串视为十六进制整数。 如果第一个字符是“1”至“9”，则将该字符串视为十进制整数。 为字母“a”到“z”（或“A”到“Z”）分配了 10 到 35 的值；仅允许分配的值小于 *base* 的字母。 超出基数范围的第一个字符停止扫描。 例如，如果*基*为 0 和扫描的第一个字符是 '0'、 假定八进制整数和一个"8"或"9"的字符将停止扫描。 **strtoumax**允许一个加号 (**+**) 或负号 (**-**) 前缀; 一个前导负号指示返回的值是 2 的补数转换后的字符串的绝对值。

## <a name="requirements"></a>要求

|例程|必需的标头|
|-------------|---------------------|
|**strtoumax**|\<stdlib.h>|
|**wcstoumax**|\<stdlib.h> 或 \<wchar.h>|
|**_strtoumax_l**|\<stdlib.h>|
|**_wcstoumax_l**|\<stdlib.h> 或 \<wchar.h>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="example"></a>示例

请参阅 [strtod](strtod-strtod-l-wcstod-wcstod-l.md) 的示例。

## <a name="see-also"></a>请参阅

[数据转换](../../c-runtime-library/data-conversion.md)<br/>
[区域设置](../../c-runtime-library/locale.md)<br/>
[localeconv](localeconv.md)<br/>
[setlocale、_wsetlocale](setlocale-wsetlocale.md)<br/>
[字符串到数值函数](../../c-runtime-library/string-to-numeric-value-functions.md)<br/>
[strtod、_strtod_l、wcstod、_wcstod_l](strtod-strtod-l-wcstod-wcstod-l.md)<br/>
[strtoimax、_strtoimax_l、wcstoimax、_wcstoimax_l](strtoimax-strtoimax-l-wcstoimax-wcstoimax-l.md)<br/>
[strtol、wcstol、_strtol_l、_wcstol_l](strtol-wcstol-strtol-l-wcstol-l.md)<br/>
[strtoul、_strtoul_l、wcstoul、_wcstoul_l](strtoul-strtoul-l-wcstoul-wcstoul-l.md)<br/>
[strtoll、_strtoll_l、wcstoll、_wcstoll_l](strtoll-strtoll-l-wcstoll-wcstoll-l.md)<br/>
[atof、_atof_l、_wtof、_wtof_l](atof-atof-l-wtof-wtof-l.md)<br/>
