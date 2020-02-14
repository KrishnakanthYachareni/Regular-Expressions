### Regular-Expressions: Regular expressions are patterns used to match character combinations in strings.
In the following tutorial JS regular expression engine is used. or use https://regexr.com/
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
#### Character Sets
1. **[] :**
`[` -> Begin a character set and `]` -> End a character set.
It mathces any one of several caharacters but only one character. Order of characters in the set does not matter. For an example `/aeiou/` matches any one vowel in text or `/gr[ea]y/` matches "grey" and "gray".
2. **Character Range :** `-`(dash) It includes all characters between two characters. For an exmaple [a-z], [A-Z], [0-9], [a-zA-Z].
Warning: [50-99] is not all numbers from 50-99. It work for only one digit ranges.
3. **Negative Character Set :** Matches not any one of several characters. Example `/[^aeiou]/` matches one consonanat(non-vowel) or `/see[^mn]/` matches "seek" and "sees" but not "seem" or "seen".
4. **Metacharacters inside character sets :** Most metacharacters inside character sets are already escaped. Do not need to escape them again. Like `/h[a.]t/` matches "hat" and "h.t", but not "hot".
5. **Shorthannd Character Sets :** 
   1. `\d` -> digit [0-9]
   2. `\w` -> Word character [a-zA-Z0-9_]  and _ (Underscore) is a word character, Hyphen is not a word character.
   3. `\s` -> White space [\t\r\n]
   4. `\D` -> Not a digit [^0-9]
   5. `\W` -> Not a Word character [^a-zA-Z0-9_]
   6. `\S` -> Not a White space [^\t\r\n]
   
#### Repetition Meta characters
1. `*` -> Preceding item, zero or more times
   1. `/apples*/` matches "apple", "apples", and "applesssssss"
2. `+` -> Preceding item, one or more times
`/.+/` matches any string of character except a line return. For  examples
   1. `/apples+/` matches "apples" and "applesssssss", but not "apple"
   2. `/Good .+\./` matches "Good Morning.", "Good day.", "Good evening." and Good night."
   3. `/\d+/` matches "90210" or any number of digits
   4. `/\s[a-z]+ed\s/` matches lowercase words ending in "ed"
   5. `/\d\d\d\d*/` matches numbers with three digits or  more
   6. `/\d\d\d*/` matches numbers with three digits or  more
3. `?` -> Preceding item, zero or one time.
   1. `/apples?/` matches "apple", "apples", but not "applesssssss"
   2. `/colou?r/` matches "color" and "colour"
4. **Quantified Repetition :** `{` -> Start quantified repetition of preceding item and `}` -> End quantified repetition of preceding item. 
   1. `{min,max}` -> min, max are positive numbers 
   2. min must always be included and can be zero. max is optional
   3. `\d{4,8}` -> matches numbers with four to eight digits.
   4. `\d{4}` -> matches numbers with exactly four digits(min is max)
   5. `\d{4,}` ->matches numbers with four or more digits{max is infinite}
   6. `\d{0,}` is same as `\d*`
   7. `\d{1,}` is same as `\d+`
   8. `/\d{3}-\d{3}-\d{4}/` matches most US phone numbers
5. **Greedy Expressions :** Expression tries to match the longest possible string to give us back as little as possible.
6. **Lazy Expressions :** use `?` to make preceding quantifier lazy
   1. `/.?[0-9]+/` -> matches "Page 266"
   2. `/.?[0-9]+?/` -> matches "Page 2" not "Page 266"
 

References:
1. Regular Expressions course content reffered from Linked Learning
   https://www.linkedin.com/learning/learning-regular-expressions-2
2.


