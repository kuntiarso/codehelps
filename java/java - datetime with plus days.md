# *Java Datetime Plus Days*

An instance how to add days to date-time. This method must return *org.joda.time.DateTime* class or similar type.

1. First way, using a simple **plusDays()** method from **DateTime** class.

   ```java
   import org.joda.time.DateTime;
   
   ...
   
   public void datePlusDays(String plusDays) {
         DateTime now = new DateTime();
         DateTime after = now.plusDays(Integer.parseInt(plusDays));
         System.out.println(after);
   }
   
   // result: 2021-07-22T13:31:11.288+08:00
   ```

2. Second way, use modifiable datetime class **MutableDateTime**, then call **addDays()** method.

   ```java
   import org.joda.time.MutableDateTime;
   import org.joda.time.DateTime;
   
   ...
   
   public void datePlusDays(String plusDays) {
         MutableDateTime now = new MutableDateTime();
         now.addDays(Integer.parseInt(plusDays));
         DateTime after = now.toDateTime();    
   }
   
   // result: 2021-07-22T13:31:11.288+08:00
   ```

That's all, hope this helps!

------

:wave: Hi, I'm @kuntiarso	:seedling: Backend Java



