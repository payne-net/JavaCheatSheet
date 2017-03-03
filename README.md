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

#### making a string uppercase and lowercase:

```
String strUpper = str1.toUpperCase();
String strUpper = str1.toUpperCase();
```

## working with data structures

#### resizing an array:

```     
int[] myArray = new int[10];

int[] tmp = new int[myArray.length + 10];
System.arraycopy(myArray, 0, tmp, 0, myArray.length);
myArray = tmp;

``` 

#### iterating over a collection:
``` 
 for (Iterator it = map.entrySet().iterator();it.hasNext();){

            Map.Entry entry = (Map.Entry)it.next();
            Object key = entry.getKey();
            Object value = entry.getValue();
        }
``` 

#### creating a mapped collection:
``` 
        HashMap map = new HashMap();
        map.put(key1,obj1);
        map.put(key2,obj2);
        map.put(key2,obj2);
``` 

#### sorting an array:
```
       int[] nums = {1,4,7,324,0,-4};
       Arrays.sort(nums);
       System.out.println(Arrays.toString(nums));
```

#### sorting an arrayList:
```
        List<String> unsortList = new ArrayList<String>();

		unsortList.add("CCC");
		unsortList.add("111");
		unsortList.add("AAA");
        Collections.sort(unsortList);
```
#### finding an object in arrayList:
```
int index = arrayList.indexOf(obj);
```
#### finding an object by value in a hashmap:
```
hashmap.containsValue(obj);
```
#### finding an object by key in a hashmap:
```
hashmap.containsKey(obj);
```
#### binary search in an array:
```
int[] nums = new int[]{7,5,1,3,6,8,9,2};
Arrays.sort(nums);
int index = Arrays.binarySearch(nums,6);
System.out.println("6 is at index: "+ index);
```
#### converting arrayList to array:
```
Object[] objects = arrayList.toArray();
```
#### converting hashmap to array:
```
Object[] objects = hashmap.entrySet().toArray();
```

## dates and times

#### printing date and time:
```
Date todaysDate = new Date(); //todays date
SimpleDateFormat formatter = new SimpleDateFormat("EEE, dd MMM yyyy HH:mm:ss"); //date format
String formattedDate = formatter.format(todaysDate);
System.out.println(formattedDate);
```

#### converting date to calendar:
```
Date mDate = new Date();
Calendar mCal = Calendar.getInstance();
mCal.setTime(mDate);
```

#### converting calendar to date:
```
Calendar mCal = Calendar.getInstance();
Date mDate = mDate.getTime();
```

#### parsing Strings into dates:
```
public void StringtoDate(String x) throws ParseException{
String date = "March 20, 1992 or 3:30:32pm";
DateFormat df = DateFormat.getDateInstance();
Date newDate = df.parse(date);
     
    }
 ```
 
#### date arithmetic using date objects:
 ``` 
Date date = new Date();
long time = date.getTime();
time += 5*24*60*60*1000; //may give a numeric overflow error on IntelliJ IDEA
Date futureDate = new Date(time);

System.out.println(futureDate);
 ```
 
#### date arithmetic using calendar objects:
 ``` 
Calendar today = Calendar.getInstance();
today.add(Calendar.DATE,5);
 ```
#### difference between two dates:
  ```
 long diff = time1 - time2;
 diff = diff/(1000*60*60*24);
  ```
#### comparing dates:
  ```
 boolean result = date1.equals(date2);
  ```
  
#### getting details from calendar:
  ```
  
Calendar cal = Calendar.getInstance();
cal.get(Calendar.MONTH);
cal.get(Calendar.YEAR);
cal.get(Calendar.DAY_OF_YEAR);
cal.get(Calendar.WEEK_OF_YEAR);
cal.get(Calendar.DAY_OF_MONTH);
cal.get(Calendar.DAY_OF_WEEK_IN_MONTH);
cal.get(Calendar.DAY_OF_MONTH);
cal.get(Calendar.HOUR_OF_DAY);
```


#### calculating the elapsed time:
 ```        
long startTime = System.currentTimeMillis();
//times flies by..
long finishTime =  System.currentTimeMillis();
long timeElapsed = startTime-finishTime;
System.out.println(timeElapsed);
```

## regular expressions

#### finding matching text using REGEX:


        


       


        
