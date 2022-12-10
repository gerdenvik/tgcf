
![image](https://user-images.githubusercontent.com/66209958/206838032-85396823-a65f-4bd3-bba2-8f9b6e566ffb.png)



Write every replacement in a new line. The original text then a colon `:` and then the new text.
```
god: devil
smart: idiot
original: new
"hello god": "whatever is ^"
```
Use quotes when you have spaces or any special character or numbers.

You can use the following special keywords to change a match to particular text formatting when regex is enabled.

`bold italics code strike plain`

Example:
- The following will make all matches of word "hello" bold  in output chat.
```
"(hello)": bold
```
- If you want to convert one text to another, and then format it, you need to use the telegram markdown syntax.
```
"(python)": "**javascript**"
```
The above example will convert all matches of word `python` into `javscript` in bold.

**Syntax**

Surround the text with special characters as mentioned.
- bold `**`
- italics `__`
- code ``` ` ```
- strike `~~`
