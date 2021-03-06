---
title: _open、_wopen | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _open
- _wopen
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _wopen
- _topen
- _open
dev_langs:
- C++
helpviewer_keywords:
- opening files, for file I/O
- topen function
- _open function
- _topen function
- _wopen function
- files [C++], opening
- wopen function
- open function
ms.assetid: 13f6a0c3-d1aa-450d-a7aa-74abc91b163e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bf1d5cca5f729e0b3e2ee55cd6d8778450bdead1
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
ms.locfileid: "32405336"
---
# <a name="open-wopen"></a>_open、_wopen

打开文件。 已弃用这些函数，因为提供了更安全的版本；请参阅 [_sopen_s、_wsopen_s](sopen-s-wsopen-s.md)。

## <a name="syntax"></a>语法

```C
int _open(
   const char *filename,
   int oflag [,
   int pmode]
);
int _wopen(
   const wchar_t *filename,
   int oflag [,
   int pmode]
);
```

### <a name="parameters"></a>参数

*filename*<br/>
文件名。

*oflag*<br/>
允许的操作类型。

*pmode*<br/>
权限模式。

## <a name="return-value"></a>返回值

其中每个函数都将为打开的文件返回文件描述符。 返回值-1 指示错误;在这种情况下**errno**设置为以下值之一。

|errno 值|条件|
|-|-|
**EACCES**|尝试打开只读文件进行写入，文件的共享模式不允许指定的操作，或给定路径是目录。
**EEXIST**|**_O_CREAT**和 **_O_EXCL**标志指定，但*filename*已存在。
**EINVAL**|无效*oflag*或*pmode*自变量。
**EMFILE**|无法使用更多的文件描述符（打开的文件太多）。
**ENOENT**|未找到文件或路径。

有关这些代码及其他返回代码的详细信息，请参阅 [errno、_doserrno、_sys_errlist 和 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)。

## <a name="remarks"></a>备注

**_Open**函数将打开指定的文件*filename* ，使其准备读取或写入，通过指定*oflag*。 **_wopen**是宽字符版本的 **_open**; *filename*参数 **_wopen**是宽字符字符串。 **_wopen**和 **_open**否则具有相同行为。

### <a name="generic-text-routine-mappings"></a>一般文本例程映射

|Tchar.h 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|
|---------------------|--------------------------------------|--------------------|-----------------------|
|**_topen**|**_open**|**_open**|**_wopen**|

*oflag*构成的一个或多个以下清单常量或常量组合，在中定义的整数表达式\<fcntl.h >。

|*oflag*常量|行为|
|-|-|
**_O_APPEND**|在执行每个写入操作之前，将文件指针移动到文件末尾。
**_O_BINARY**|在二进制（未转换）模式下打开该文件。 （有关二进制模式的说明，请参阅 [fopen](fopen-wfopen.md)。）
**_O_CREAT**|创建文件并打开它以供写入。 如果指定的文件不起作用*filename*存在。 *Pmode*时，参数是必需 **_O_CREAT**指定。
**_O_CREAT** &AMP;#124; **_O_SHORT_LIVED**|创建一个文件作为临时文件，如果可能，请不要将它刷新到磁盘中。 *Pmode*时，参数是必需 **_O_CREAT**指定。
**_O_CREAT** &AMP;#124; **_O_TEMPORARY**|创建一个文件作为临时文件；在关闭最后一个文件描述符时，删除该文件。 *Pmode*时，参数是必需 **_O_CREAT**指定。
**_O_CREAT**&AMP;#124; ` _O_EXCL`|如果由指定的文件，则返回一个错误值*filename*存在。 仅当与一起使用时应用 **_O_CREAT**。
**_O_NOINHERIT**|阻止创建共享文件描述符。
**_O_RANDOM**|指定缓存针对（但不限于）从磁盘的随机访问进行优化。
**_O_RDONLY**|打开文件以供只读。 不能与指定 **_O_RDWR**或 **_O_WRONLY**。
**_O_RDWR**|打开文件以供读取和写入。 不能与指定 **_O_RDONLY**或 **_O_WRONLY**。
**_O_SEQUENTIAL**|指定缓存针对（但不限于）从磁盘的顺序访问进行优化。
**_O_TEXT**|在文本（转换）模式下打开文件。 （有关详细信息，请参阅[文本和二进制模式文件 I/O](../../c-runtime-library/text-and-binary-mode-file-i-o.md) 和 [fopen](fopen-wfopen.md)。）
**_O_TRUNC**|打开文件并将其长度截断为零；该文件必须具有写入权限。 不能与指定 **_O_RDONLY**。 **_O_TRUNC**用于 **_O_CREAT**打开一个现有文件或创建一个文件。 **注意：** **_O_TRUNC**标志会损坏指定文件的内容。
**_O_WRONLY**|打开文件以供只写。 不能与指定 **_O_RDONLY**或 **_O_RDWR**。
**_O_U16TEXT**|在 Unicode UTF-16 模式下打开文件。
**_O_U8TEXT**|在 Unicode UTF-8 模式下打开文件。
**_O_WTEXT**|在 Unicode 模式下打开文件。

若要指定文件访问模式，你必须指定 **_O_RDONLY**， **_O_RDWR**，或 **_O_WRONLY**。 对于访问模式，不存在默认值。

如果 **_O_WTEXT**用于打开文件进行读取， **_open**读取文件的开头，并检查字节顺序标记 (BOM)。 如果存在 BOM，则将该文件视为 UTF-8 或 UTF-16LE，具体取决于该 BOM。 如果不存在 BOM，则将该文件视为 ANSI。 通过使用以进行写入打开文件时 **_O_WTEXT**，使用 utf-16。 无需考虑任何以前的设置或字节顺序标记，如果 **_O_U8TEXT**是使用，打开文件时始终为 utf-8; **_O_U16TEXT**是使用，始终作为 utf-16 打开该文件。

通过使用在 Unicode 模式下打开文件时 **_O_WTEXT**， **_O_U8TEXT**，或 **_O_U16TEXT**、 输入函数将从文件读取到 utf-16 数据的数据转换存储类型为**wchar_t**。 写入到在 Unicode 模式下打开的文件的函数需要包含存储为类型的 utf-16 数据的缓冲区**wchar_t**。 如果将文件编码为 UTF-8，则在写入它时，UTF-16 数据会转换为 UTF-8；在读取它时，该文件的 UTF-8 编码的内容会转换为 UTF-16。 尝试在 Unicode 模式下读取或写入奇数个字节会导致参数验证错误。 若要读取或写入在你的程序中存储为 UTF-8 的数据，请使用文本或二进制文件模式，而不是 Unicode 模式。 你应负责所有必需的编码转换。

如果 **_open**使用调用 **_O_WRONLY** | **_O_APPEND** （追加模式） 和 **_O_WTEXT**， **_O_U16TEXT**，或 **_O_U8TEXT**，它首先尝试打开文件进行读取和写入、 读取 BOM，然后重新打开它供只写。 如果无法打开该文件以供读取和写入，则它将打开该文件以供只写，并使用 Unicode 模式设置的默认值。

当两个或多个清单常量来形成*oflag*自变量，这些常量将与按位 OR 运算符合并 ( **&#124;** )。 有关二进制模式和文本模式的讨论，请参阅[文本和二进制模式文件 I/O](../../c-runtime-library/text-and-binary-mode-file-i-o.md)。

*Pmode*参数是必需的仅当 **_O_CREAT**指定。 如果该文件已存在， *pmode*将被忽略。 否则为*pmode*指定第一次关闭新文件时设置的文件权限设置。 **_open**将当前文件权限掩码应用到*pmode*之前设置了权限。 (有关详细信息，请参阅[_umask](umask.md)。)*pmode*是一个包含一个或两个中定义的以下清单常量的整数表达式\<sys\stat.h >。

|*pmode*|含义|
|-|-|
**_S_IREAD**|只允许读取。
**_S_IWRITE**|允许写入。 （实际上，允许读取和写入。）
**_S_IREAD** &AMP;#124; **_S_IWRITE**|允许读取和写入。

当给定这两个常量时，它们是否联接使用按位 OR 运算符 ( **&#124;** )。 在 Windows 中，所有文件均可读；不会提供只写权限。 因此，模式 **_S_IWRITE**和 **_S_IREAD** | **_S_IWRITE**是等效的。

如果以外的某种组合的值 **_S_IREAD**和 **_S_IWRITE**为指定*pmode*— 即使它会指定一个有效*pmode*在另一个操作系统-如果除了允许之外的任何值或*oflag*指定值，该函数将在调试模式下生成断言，并调用无效参数处理程序，如中所述[参数验证](../../c-runtime-library/parameter-validation.md)。 如果允许执行继续，函数将返回-1 并设置**errno**到**EINVAL**。

## <a name="requirements"></a>要求

|例程|必需的标头|可选标头|
|-------------|---------------------|---------------------|
|**_open**|\<io.h>|\<fcntl.h>、\<sys\types.h>、\<sys\stat.h>|
|**_wopen**|\<io.h> 或 \<wchar.h>|\<fcntl.h>、\<sys\types.h>、\<sys\stat.h>|

**_open**和 **_wopen**是 Microsoft 扩展。 有关更多兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="libraries"></a>库

[C 运行时库](../../c-runtime-library/crt-library-features.md)的所有版本。

## <a name="example"></a>示例

```C
// crt_open.c
// compile with: /W3
/* This program uses _open to open a file
* named CRT_OPEN.C for input and a file named CRT_OPEN.OUT
* for output. The files are then closed.
*/
#include <fcntl.h>
#include <sys/types.h>
#include <sys/stat.h>
#include <io.h>
#include <stdio.h>

int main( void )
{
   int fh1, fh2;

   fh1 = _open( "CRT_OPEN.C", _O_RDONLY ); // C4996
   // Note: _open is deprecated; consider using _sopen_s instead
   if( fh1 == -1 )
      perror( "Open failed on input file" );
   else
   {
      printf( "Open succeeded on input file\n" );
      _close( fh1 );
   }

   fh2 = _open( "CRT_OPEN.OUT", _O_WRONLY | _O_CREAT, _S_IREAD |
                            _S_IWRITE ); // C4996
   if( fh2 == -1 )
      perror( "Open failed on output file" );
   else
   {
      printf( "Open succeeded on output file\n" );
      _close( fh2 );
   }
}
```

### <a name="output"></a>输出

```Output
Open succeeded on input file
Open succeeded on output file
```

## <a name="see-also"></a>请参阅

[低级别 I/O](../../c-runtime-library/low-level-i-o.md)<br/>
[_chmod、_wchmod](chmod-wchmod.md)<br/>
[_close](close.md)<br/>
[_creat、_wcreat](creat-wcreat.md)<br/>
[_dup、_dup2](dup-dup2.md)<br/>
[fopen、_wfopen_wfopen](fopen-wfopen.md)<br/>
[_sopen、_wsopen](sopen-wsopen.md)<br/>
