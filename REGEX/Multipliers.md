# Multipliers

You can use braces to put a multiplier after a literal or a character class.

- The regular expression a{1} is the same as a and means "find an a".
- a{3} means "find an a followed by an a followed by an a".
- a\{2\} means "find an a followed by a left brace followed by a 2 followed by a right brace".
- Braces have no special meaning inside character classes. [{}] means "find a left brace or a right brace".

Multipliers may have ranges:

- x{4,4} is the same as x{4}.
- colou{0,1}r means "find colour or color".
- a{3,5} means "find aaaaa or aaaa or aaa".

Note that the longer possibility is most preferred, because multipliers are greedy. If your input text is I had an aaaaawful day then this regular expression will find the aaaaa in aaaaawful. It won't just stop after three as.

The multiplier is greedy, but it won't disregard a perfectly good match. If your input text is I had an aaawful daaaaay, then this regular expression will find the aaa in aaawful on its first match. Only if you then say "find me another match" will it continue searching and find the aaaaa in daaaaay.

Multiplier ranges may be open-ended:

- `a{1,}` means "find one or more as in a row". Your multiplier will still be greedy, though. After finding the first a, it will try to find as many more as as possible.
- `.{0,}` means "find anything". No matter what your input text is - even the empty string - this regular expression will successfully match the entire text and return it to you.

Freebee multipliers

- ? means the same as {0,1}. For example, colou?r means "find colour or color".
- * means the same as {0,}. For example, .* means "find anything", exactly as above.
- + means the same as {1,}. For example, \w+ means "find a word". Here a "word" is a sequence of 1 or more "word characters", such as _var or AccountName1.
