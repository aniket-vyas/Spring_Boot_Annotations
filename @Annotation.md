# @Entity

- It specifies that the class is an entity & is mapped to Data Base table.
- Class name must be same as table name.

```java
@Entity
public class Student {

}
```

# @Id

- It specifies the primary key on an entity.

```java
@Entity
public class Student {

  @Id
  private int id;
  private String name;
  private String course;

}
```

# @GeneratedValue

- Use for auto increment.

```java
@Entity
public class Student {

  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private int id;
  private String name;
  private String course;

}
```

# @Autowired

- Acts like "new" keyword for creating bean (object).
- It is used to autowire spring bean on setter methods, instance variable, and constructor.
- When we use @Autowired annotation, the spring container auto-wires the bean by matching data-type.

```java
@Entity
public class Student {

  @Autowired
  private Student stu;
  
  // @Autowired create a bean of class "Student" and store the address in "stu"

}
```

# @Test

- It is an annotation of junit which helps us to run the methods & also check the code inside methods , if any code fails it will report a faliure.
- It works only on non-static methods.
- No object , No method calling , No main() method.

            # junit is a Unit Testing (White Box Testing) framework --> testing which is done at code level 

```java
import org.junit.*;
public class Student {

  @Test
  public void test() {
    System.Out.Println(" from test ");
  }

}
```

# @Before

- It will run before every test() method.
- It works only on non-static methods.

```java
import org.junit.*;
public class Student {

  @Test
  public void test1() {
    System.Out.Println(" from test - 1 ");
  }
  
  @Test
  public void test2() {
    System.Out.Println(" from test - 2 ");
  }
  
  @Before
  public void test3() {
    System.Out.Println(" from before ");
  }
  
}

```

    # OUTPUT :-

     from before
     from test - 1
     from before
     from test - 2


# @After

- It will run after every test() method.
- It works only on non-static method.

```java
import org.junit.*;
public class Student {

  @Test
  public void test1() {
    System.Out.Println(" from test - 1 ");
  }
  
  @Test
  public void test2() {
    System.Out.Println(" from test - 2 ");
  }
  
  @Before
  public void test3() {
    System.Out.Println(" from before ");
  }
  
  @After
  public void test4() {
    System.Out.Println(" from after ");
  }
  
}
```

    # OUTPUT :-

     from before
     from test - 1
     from after
     from before
     from test - 2
     from after


# @BeforeClass

- It will applied only on static method.
- It will run only once.
- It will run before all methods.

```java
import org.junit.*;
public class Student {

  @Test
  public void test1() {
    System.Out.Println(" from test - 1 ");
  }
  
  @Test
  public void test2() {
    System.Out.Println(" from test - 2 ");
  }
  
  @Before
  public void test3() {
    System.Out.Println(" from before ");
  }
  
  @After
  public void test4() {
    System.Out.Println(" from after ");
  }
  
  @BeforeClass
  public static void test5() {
    System.Out.Println(" from BeforeClass ");
  }
  
}
```

    # OUTPUT :-

     from BeforeClass
     from before
     from test - 1
     from after
     from before
     from test - 2
     from after


# @AfterClass

- It will applied only on static method.
- It will run only once.
- It will run after all methods.

```java
import org.junit.*;
public class Student {

  @Test
  public void test1() {
    System.Out.Println(" from test - 1 ");
  }
  
  @Test
  public void test2() {
    System.Out.Println(" from test - 2 ");
  }
  
  @Before
  public void test3() {
    System.Out.Println(" from before ");
  }
  
  @After
  public void test4() {
    System.Out.Println(" from after ");
  }
  
  @BeforeClass
  public static void test5() {
    System.Out.Println(" from BeforeClass ");
  }
  
  @AfterClass
  public static void test6() {
    System.Out.Println(" from AfterClass ");
  }
  
}
```

    # OUTPUT :-

     from BeforeClass
     from before
     from test - 1
     from after
     from before
     from test - 2
     from after
     from AfterClass
