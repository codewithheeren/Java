## OOPS - Aggregation
### AggregationMainClass.java

```java
/**
 * Implementation of Aggregation
 * @author Heeren
 * @version 1.0
 */
package com.java.oops8;
import java.util.ArrayList;
import java.util.List;

class Employee {
    String name;
    int id;

    Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    @Override
    public String toString() {
        return "Employee{name='" + name + "', id=" + id + "}";
    }
}

class Department {
    String name;
    List<Employee> employees;

    Department(String name) {
        this.name = name;
        this.employees = new ArrayList<>();
    }

    void addEmployee(Employee employee) {
        employees.add(employee);
    }

    void showEmployees() {
        System.out.println("Department: " + name);
        for (Employee employee : employees) {
            System.out.println(employee);
        }
    }
}

public class AggregationMainClass {
    public static void main(String[] args) {
        Employee employee1 = new Employee("John", 1);
        Employee employee2 = new Employee("Alice", 2);
        
        Department department = new Department("HR");
        department.addEmployee(employee1);
        department.addEmployee(employee2);
        
        department.showEmployees();
    }
}

```
---
