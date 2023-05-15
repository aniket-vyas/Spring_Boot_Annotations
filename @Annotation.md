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
















