# *Java Date to String*

An instance how to convert date to string with formatter. This method must return *java.lang.String* class type.

1. Using **SimpleDateFormat** class.

   ```java
   import java.text.SimpleDateFormat;
   
   ...
   
   public void dateToString(Date date) {
       SimpleDateFormat formatter = new SimpleDateFormat("yyyyMMddHHmmssSSS");
       String dateStr = formatter.format(date);
       System.out.println(dateStr);
       
       formatter = new SimpleDateFormat("yyyy-MM-dd");
       dateStr = formatter.format(date);
       System.out.println(dateStr);
   }
   
   // result: 20210523123258133
   // result: 2021-05-23
   ```


That's all, hope this helps!

------

:wave: Hi, I'm @kuntiarso	:seedling: Backend Java

