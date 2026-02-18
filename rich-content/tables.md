# Table Tests

## Simple Table

| Name    | Age | City    |
| ------- | --- | ------- |
| Alice   | 30  | NYC     |
| ​       | ​   | ​       |
| Bob     | 25  | LA      |
| Charlie | 35  | Chicago |

## Aligned Table

| Left | Center | Right |
| ---- | ------ | ----- |
| L1   | C1     | R1    |
| L2   | C2     | R2    |
| L3   | C3     | R3    |

## Wide Table

| Column 1 | Column 2 | Column 3 | Column 4 | Column 5 | Column 6 | Column 7 | Column 8 | Column 9 | Column 10 |
| -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | --------- |
| Data     | Data     | Data     | Data     | Data     | Data     | Data     | Data     | Data     | Data      |
| More     | More     | More     | More     | More     | More     | More     | More     | More     | More      |

## Table with Formatting

| Feature                                      | Status | Notes        |
| -------------------------------------------- | ------ | ------------ |
| **Bold**                                     | ✅      | Works great  |
| _Italic_                                     | ✅      | Also works   |
| `Code`                                       | ✅      | Inline code  |
| ~~Strike~~                                   | ⚠️     | Partial      |
| ​<br/>​                                      | ✅      | Clickable    |
| ![img](https://via.placeholder.com/20 "img") | ❓      | Inline image |

## Table with Long Content

| Short | Very Long Content Column                                                                                                                   |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A     | This cell contains a very long piece of text that might cause the table to overflow or wrap in interesting ways depending on the renderer. |
| B     | Another long cell with **bold**, _italic_, and `code` mixed in to test formatting in long table cells.                                     |

## Single Column Table

| Items |
| ----- |
| One   |
| Two   |
| Three |

## Table with Empty Cells

| A | B | C |
| - | - | - |
| 1 | ​ | 3 |
| ​ | 2 | ​ |
| 1 | 2 | 3 |

## Minimal Table

| A | B |
| - | - |
| 1 | 2 |

## Table with Pipes in Content

| Expression  | Result |
| ----------- | ------ |
| `a \| b`    | OR     |
| `echo "hi"` | hi     |
