# *Java Datetime to String*

An instance how to convert datetime to string with formatter. This method must return *java.lang.String* class type.

1. Using **DateTimeFormatter** class from **Joda-Time** package. It has **print** method which will convert datetime to string.

   ```java
   import org.joda.time.format.DateTimeFormatter;
   import org.joda.time.format.DateTimeFormat;
   import org.joda.time.DateTime;
   
   ...
   
   public void dateToString(DateTime now) {
         DateTimeFormatter formatter = DateTimeFormat.forPattern("yyyy-MM-dd HH:mm:ss");
         String datetimeStr = formatter.print(now);
         System.out.println(datetimeStr);
       
         formatter = DateTimeFormat.forPattern("MM/dd/YYYY");
         datetimeStr = formatter.print(now);
         System.out.println(datetimeStr);
   }
   
   // result1: 2021-05-23 21:50:34
   // result2: 05/23/2021
   ```

That's all, hope this helps!

------

:wave: Hi, I'm @kuntiarso	:seedling: Backend Java

