# JavaCheatSheet

## string manupilation 



#### comparing strings:
```
boolean result = str1.equals(str2);
boolean result = str1.equalsIgnoreCase(str2);
```

#### searching and rerieving substrings:

```
int result = str1.indexOf(str2);
int result = str1.indexOf(str2,5);
String index = str1.substring(14);
```

#### processing a string one character at a time:
```
for (int i=0;i<str1.length();i++){

char aChar = str1.charAt(i);
}
```

#### Reversing a String by Character:

```

public class Main {

    public static void main(String[] args) {

        String str1 = "whatever string something";

        StringBuffer str1buff = new StringBuffer(str1);

        String str1rev = str1buff.reverse().toString();

        System.out.println(str1rev);


    }
}
```


#### Reversing a String by Word:
```

public class Main {

public static void main(String[] args) {

    String str1 = "reverse this string";

    Stack<Object> stack = new Stack<>();

    StringTokenizer strTok = new StringTokenizer(str1);

    while(strTok.hasMoreTokens()){

        stack.push(strTok.nextElement());
    }

    StringBuffer str1rev = new StringBuffer();

    while(!stack.empty()){

        str1rev.append(stack.pop());
        str1rev.append(" ");


    }

    System.out.println(str1rev);



}
}
```



#### making a string upper or lowercase:
```


String strUpper = str1.toUpperCase();
String strLower = str1.toLowerCase();
```


#### removing end and start spaces:
```

String str1 = "     asdfsdf   ";
str1.trim(); //asdfsdf
```

#### removing all spaces:
```
str1.replace(" ","");
```

#### parsing a comma seperated string:

```
String str = "tim,kerry,timmy,camden";
String[] results = str.split(",");
```
