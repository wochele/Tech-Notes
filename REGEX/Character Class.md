# The character class

- A character class is a collection of characters in square brackets. This means, "find any one of these characters".
    - The regular expression c[aeiou]t means, "find a c followed by a vowel followed by a t". In a piece of text, this will find cat, cet, cit, cot and cut.
    - The regular expression [0123456789] means "find a digit".
    - The regular expression [a] means the same as a: "find an a".
    - The regular expression [ ] means "find a space".
- Outside of a character class, the hyphen has no special meaning. The regular expression a-z means "find an a followed by a hyphen followed by a z".
- Ranges and isolated characters may coexist in the same character class:
    - [0-9.,] means "find a digit or a full stop or a comma".
    - [0-9a-fA-F] means "find a hexadecimal digit".
    - [a-zA-Z0-9\-] means "find an alphanumeric character or a hyphen".
- Character class negation - You may negate a character class by putting a caret at the very beginning.
    - \[^a\] means "find any character other than an a".
    - \[^a-zA-Z0-9\] means "find a non-alphanumeric character".
    - \[\^abc\] means "find a caret or an a or a b or a c".
    - \[^\^\] means "find any character other than a caret". (Ugh!)
- Freebie character classes
    - \d means the same as [0-9]: "find a digit". (To find a backslash followed by a d, use the regular expression \\d.)
    - \w means the same as [0-9A-Za-z_]: "find a word character".
    - \s means "find a space character (space, tab, carriage return or line feed)".
    - \D means [^0-9]: "find a non-digit".
    - \W means [^0-9A-Za-z_]: "find a non-word character".
    - \S means "find a non-space character".

