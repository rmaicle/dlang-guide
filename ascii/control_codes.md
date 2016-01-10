---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: ASCII Characters
section: Control Codes
excerpt:
group: DLang
tags: [dlang, dguide, draft]
---

> In computing and telecommunication, a control character or non-printing character is a code point (a number) in a character set, that does not represent a written symbol. They are used as in-band signaling to cause effects other than the addition of a symbol to the text. All other characters are mainly printing, printable, or graphic characters, except perhaps for the "space" character (see ASCII printable characters).
>
> All entries in the ASCII table below code 32 (technically the C0 control code set) are of this kind, including CR and LF used to separate lines of text. The code 127 (DEL) is also a control character. Extended ASCII sets defined by ISO 8859 added the codes 128 through 159 as control characters, this was primarily done so that if the high bit was stripped it would not change a printing character to a C0 control code, but there have been some assignments here, in particular NEL. This second set is called the C1 set.
>
> These 65 control codes were carried over to Unicode. Unicode added more characters that could be considered controls, but it makes a distinction between these "Formatting characters" (such as the Zero-width non-joiner), and the 65 Control characters.
>
> The Extended Binary Coded Decimal Interchange Code (EBCDIC) character set contains 65 control codes, including all of the ASCII control codes as well as additional codes which are mostly used to control IBM peripherals.

The following table shows the ASCII control code chart.

| Binary  | Oct | Dec | Hex | Abbr | Caret notation | Escape code | Name |
|:-------:|:---:|:---:|:---:|:----:|:--------------:|:-----------:|------|
| 0000000 | 000 |   0 |  00 | NUL  | &#94;@         |     \0      | Null character
| 0000001 | 001 |   1 |  01 | SOH  | &#94;A         |             | Start of Header
| 0000010 | 002 |   2 |  02 | STX  | &#94;B         |             | Start of Text
| 0000011 | 003 |   3 |  03 | ETX  | &#94;C         |             | End of Text
| 0000100 | 004 |   4 |  04 | EOT  | &#94;D         |             | End of Transmission
| 0000101 | 005 |   5 |  05 | ENQ  | &#94;E         |             | Enquiry
| 0000110 | 006 |   6 |  06 | ACK  | &#94;F         |             | Acknowledgment
| 0000111 | 007 |   7 |  07 | BEL  | &#94;G         |     \a      | Bell
| 0001000 | 010 |   8 |  08 | BS   | &#94;H         |     \b      | Backspace[d][e]
| 0001001 | 011 |   9 |  09 | HT   | &#94;I         |     \t      | Horizontal Tab[f]
| 0001010 | 012 |  10 |  0A | LF   | &#94;J         |     \n      | Line feed
| 0001011 | 013 |  11 |  0B | VT   | &#94;K         |     \v      | Vertical Tab
| 0001100 | 014 |  12 |  0C | FF   | &#94;L         |     \f      | Form feed
| 0001101 | 015 |  13 |  0D | CR   | &#94;M         |     \r      | Carriage return[g]
| 0001110 | 016 |  14 |  0E | SO   | &#94;N         |             | Shift Out
| 0001111 | 017 |  15 |  0F | SI   | &#94;O         |             | Shift In
| 0010000 | 020 |  16 |  10 | DLE  | &#94;P         |             | Data Link Escape
| 0010001 | 021 |  17 |  11 | DC1  | &#94;Q         |             | Device Control 1 (oft. XON)
| 0010010 | 022 |  18 |  12 | DC2  | &#94;R         |             | Device Control 2
| 0010011 | 023 |  19 |  13 | DC3  | &#94;S         |             | Device Control 3 (oft. XOFF) 
| 0010100 | 024 |  20 |  14 | DC4  | &#94;T         |             | Device Control 4
| 0010101 | 025 |  21 |  15 | NAK  | &#94;U         |             | Negative Acknowledgment
| 0010110 | 026 |  22 |  16 | SYN  | &#94;V         |             | Synchronous idle
| 0010111 | 027 |  23 |  17 | ETB  | &#94;W         |             | End of Transmission Block
| 0011000 | 030 |  24 |  18 | CAN  | &#94;X         |             | Cancel
| 0011001 | 031 |  25 |  19 | EM   | &#94;Y         |             | End of Medium
| 0011010 | 032 |  26 |  1A | SUB  | &#94;Z         |             | Substitute
| 0011011 | 033 |  27 |  1B | ESC  | &#94;[         |    \e[h]    | Escape[i]
| 0011100 | 034 |  28 |  1C | FS   | &#94;\         |             | File Separator
| 0011101 | 035 |  29 |  1D | GS   | &#94;]         |             | Group Separator
| 0011110 | 036 |  30 |  1E | RS   | &#94;&#94;[j]  |             | Record Separator
| 0011111 | 037 |  31 |  1F | US   | &#94;&#95;     |             | Unit Separator
| 1111111 | 177 | 127 |  7F | DEL  | &#94;?         |             | Delete[k][e]
