# *Java Date Plus Days*

An instance how to add days to java date. This method must return *java.util.Date* class type.

1. First way, using **DateUtils** class from **Apache Commons** package.

   ```java
   import java.util.*;
   import org.apache.commons.lang3.time.DateUtils;
   
   ...
   
   public void datePlusDays(String plusDays) {
         Date now = new Date();
         Date after = DateUtils.addDays(now, Integer.parseInt(plusDays));
         System.out.println(after);
   }
   
   // result: Wed May 25 12:59:57 ICT 2021
   ```

2. Second way, using **Calendar** class.

   ```java
   import java.util.*;
   
   ...
   
   public void datePlusDays(String plusDays) {
         Calendar calendar = Calendar.getInstance(); 
         calendar.add(Calendar.DATE, Integer.parseInt(plusDays));
       
         Date after = calendar.getTime();
         System.out.println(after);
   }
   
   // result: Wed May 25 12:59:57 ICT 2021
   ```

That's all, hope this helps!

------

:wave: Hi, I'm @kuntiarso	:seedling: Backend Java



