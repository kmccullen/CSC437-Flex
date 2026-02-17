Given this BNF:

<expression> ::= <term> <expression_prime>
<expression_prime> ::= "+" <term> <expression_prime> | ""
<term> ::= <factor> <term_prime>
<term_prime> ::= "*" <factor> <term_prime> | ""
<factor> ::= "(" <expression> ")" | <id>
<id> ::= <int> | <variable>

An integer is defined as usual (sequence of digits 0..9)
A variable can be any string starting with a-z, followed by up to 7 more letters (a-z) or numbers (0-9)

You can limit the length of a regular expression by using {m,n} as a suffix, which says m to n digits in length.

Write the flex input file to tokenize this grammar. Build the flex tokenizer, and tokenize the provided examples.

Submit your flex input file, your lex.yy.c, and the result of running your program on the supplied input.
