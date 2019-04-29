# String Splosion

Given a non-empty string like "Code" return a string like "CCoCodCode".

```
stringSplosion("Code") → "CCoCodCode"
stringSplosion("abc") → "aababc"
stringSplosion("ab") → "aab"
```

## Java
```java
public String stringSplosion(String str) {
  String newStr = "";
  int strLen = str.length(); // So we wouldn't have to repeatedly query the length
  
  for (int i = 0; i < strLen; i++) {
    newStr += str.substring(0, i + 1);
  }
  
  return newStr;
}
```
