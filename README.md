# COMP-SCI-2000-7081 专业辅导

# VX: csprojhelp 备注: github

Nand2Tetris

HDL Hach Assembly VM Stack Jack Language OS

Mux Alu Adder Dff zx nx zy ny f no out

A-instruction

C-instruction

Parser 
Lexical Elements

keyword

symbol

::= ’class’ | ’constructor’ | ’function’ | ’method’ | \ ’field’ | ’static’ | ’var’ | ’int’ | ’char’ | \ ’boolean’ | ’void’ | ’true’ | ’false’ | ’null’ | \ ’this’ | ’let’ | ’do’ | ’if’ | ’else’ | ’while’ | \ ’return’

::=

’{’

|

’}’

|

’(’

|

’)’

|

’[’

|

’]’

|

’.’

|

\

’,’ | ’;’ | ’+’ | ’-’ | ’*’ | ’/’ | ’&’ | \

’|’ | ’<’ | ’>’ | ’=’ | ’~’ | ’

integerConstant ::= A decimal number in the range 0 .. 32767 stringConstant ::= ’"’ A sequence of Unicode characters not including double quote or newline ’"’ identifier ::= A sequence of letters, digits and underscore (’_’) not starting with a digit.

Statements

statements statement

letStatement ifStatement

::= statement* ::= letStatement | ifStatement | whileStatement | \ doStatement | returnStatement}

::=

’let’

varName

(’[’

expression

’]’)?

’=’

expression

’;’

::= ’if’ ’(’ expression ’)’ ’{’ statements ’}’ \ (’else’ ’{’ statements ’}’)?

whileStatement ::= ’while’ ’(’ expression ’)’ ’{’ statements ’}’ doStatement ::= ’do’ subroutineCall ’;’ returnStatement ::= ’return’ expression? ’;’

Expressions

expression term

subroutineCall

::= term (op term)* ::= integerConstant | stringConstant | \

keywordConstant | varName | \

varName ’[’ expression ’]’ | subroutineCall | \

’(’ expression ’)’ | unaryOp term ::= subroutineName ’(’ expressionList ’)’ | \

(className | varName) ’.’ subroutineName ’(’ expressionList ’)’ ::= (expression (’,’ expression)*)?

expressionList op unaryOp keywordConstant ::= ’true’ | ’false’ | ’null’ | ’this’ varName ::= identifier
