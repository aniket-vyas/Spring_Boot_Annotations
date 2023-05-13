# @Required

1. Checks if a particular property has been set or not.

```java
public class Machine {  

  private Integer cost;  
  
  @Required  
  public void setCost(Integer cost) {  
    this.cost = cost;  
  }  
  
  public Integer getCost() {  
    return cost;  
  }  
  
}  
```
