### Regular-Expressions: Regular expressions are patterns used to match character combinations in strings.
In the following tutorial Java regular expression engine has been used. or use https://regexr.com/
By default regular expresions are case sensitive.
#### Modes
1. **Standard :** `/re/` re -> regular expression
2. **Global :** `/re/g` g -> global says match this over and over and over again throughout the document.
3. **Case Insensitive :** `/re/i`
4. **Multi Line :** `/re/m` m -> more than one line check
#### Meta Characters
1. **Wildcard :** `.` (dot) any character excpet new line. wild card is only one single character. for an example `/h/t` matches "hat", "hot", "hit" but not "heat".
2. **Escape Character** `\` (backslash) escape the next character and it allows use of meta characters as literal characters. for an example `/9\.00/` matches 9.00 not 9500, 9-00
quotation marks are not meta characters & can't be escaped.
3. **Special Characters :** spaces are normal space ` `, Tabs `\t` and Line returns `\r` or `\n` or `\r\n` these are specific to operating system.



















References:
1. Regular Expressions course content reffered from Linked Learning
   https://www.linkedin.com/learning/learning-regular-expressions-2
2.


