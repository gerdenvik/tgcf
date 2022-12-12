
![image](https://user-images.githubusercontent.com/66209958/206838032-85396823-a65f-4bd3-bba2-8f9b6e566ffb.png)



Write every replacement in a new line. The original text then **a colon `:`** and then **a space** and then the new text.
```
god: devil
smart: idiot
original: new
"hello god": "whatever is ^"
'some regex with \ character': 'new expression'
```
Use quotes when you have spaces or any special character or numbers. 

- Its recommended to use **single quotes**. Quotes are must when your string contain spaces or special characters.
- Double quotes wont work if your regex contains `\`.
- The text you enter is parsed as yaml. So should follow yaml rules. 
- The key-value pairs must be string and string.


### Remove certain piece of text
For that, you need to put a blank string in place of new text. Like nothing within double quotes. `""`.
```
"evil": ""
```
By this, all occurrences of `evil` in your message will be removed.

#### Remove URLs
```
'(@|www|http?)\S+': ''
```
[Visit regex101](https://regex101.com/r/46KTQC/1) to test or understand the regex.

### Format text using Replace Plugin

#### Case 1. Change the format of matching text
You can use the following special keywords to change a match to particular text formatting when regex is enabled.

`bold italics code strike plain`

Example:
- The following will make all matches of word "hello" bold  in output chat.
```
"(hello)": bold
```

#### Case 2. Convert a match to another text, and then have special formatting for it
If you want to convert one text to another, and then format it, you need to use the telegram markdown syntax.
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
