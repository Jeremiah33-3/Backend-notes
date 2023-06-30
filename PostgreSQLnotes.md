# [Documentation](https://www.postgresql.org/docs/)

things I find useful

## [Pattern matching](https://www.postgresql.org/docs/current/functions-matching.html)

three things:
1. LIKE expression
2. SIMILAR expression
3. POSIX regular expression

`string LIKE pattern [ESCAPE escape-character]
string NOT LIKE pattern [ESCAPE escape-character]`

The LIKE expression 
- returns true if the string matches the supplied pattern.
- As expected, the NOT LIKE expression returns false if LIKE returns true, and vice versa. An equivalent expression is NOT (string LIKE pattern).
- If pattern does not contain percent signs or underscores, then the pattern only represents the string itself; in that case LIKE acts like the equals operator. An underscore (_) in pattern stands for (matches) any single character; a percent sign (%) matches any sequence of zero or more characters.
- always cover entire string
- to match a literal underscore of percent sign, an ESCAPE sign must precede. The default escape character is the backslash but a different one can be selected by using the ESCAPE clause. To match the escape character itself, write two escape characters.
- The key word ILIKE can be used instead of LIKE to make the match _case-insensitive_ according to the active locale. Not in the SQL standard but is a PostgreSQL extension.

`string SIMILAR TO pattern [ESCAPE escape-character]
string NOT SIMILAR TO pattern [ESCAPE escape-character]`

The SIMILAR expression
- returns true or false depending on whether its pattern matches the given string
- imilar to LIKE, except that it interprets the pattern using the **SQL standard's definition of a regular expression**
- SIMILAR TO operator succeeds only if its pattern matches the entire string (similar to LIKE); unlike common regular expression behavior where the pattern can match any part of the string
- SIMILAR TO uses _ and % as wildcard characters denoting any single character and any string, respectively (these are comparable to . and .* in POSIX regular expressions).
- unlike LIKE, SIMILAR TO supports these pattern-matching metacharacters borrowed from POSIX regular expressions
  - | denotes alternation (either of two alternatives).
  - \* denotes repetition of the previous item zero or more times.
  - \+ denotes repetition of the previous item one or more times.
  - \? denotes repetition of the previous item zero or one time.
  - \{m} denotes repetition of the previous item exactly m times.
  - \{m,} denotes repetition of the previous item m or more times.
  - \{m,n} denotes repetition of the previous item at least m and not more than n times.
  - Parentheses () can be used to group items into a single logical item.
  - A bracket expression [...] specifies a character class, just as in POSIX regular expressions.
- As with LIKE, a backslash disables the special meaning of any of these metacharacters

POSIX regular expressions (refer to docs)
