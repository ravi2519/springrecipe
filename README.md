# Spring Receipe

1. <strong>OneToOne relationships</strong><br>
    Two entities as <code>Notes</code> and <code>Receipe</code> added. <br>
   Both have OneToOne mapping. <code>Receipe</code> is set with cascade all while <code>Notes</code> doesn't have any cascade type. <br>
   All these entities are having Id as <code>GeneratedValue</code> using </code>Identity</code>.
    
2. <strong>OneToMany and ManyToOne relationships</strong><br> 
    Next we have added one more entity called <code>Ingredient</code>.<br>
    This entity has ManyToOne relationship with <code>Receipe</code> and vice versa.</br>
    The cascading is set to <code>All</code> in <code>Receipe</code> while we don't have any cascading defined for <code>receipe</code> in <code>Ingredient</code>.<br>
    The <code>mappedBy</code> is defined for <code>receipe</code> instance variable.  
    
3. <strong>JPA Enumerations</strong><br>
    Added an <code>Enum</code> class called <code>Difficulty</code>. <br>
    To store java enums into database we have a JPA annotation called <code>@Enumerated</code><br>
    Now this annotation has two type - <code>ORDINAL</code> and <code>STRING</code>.<br>
    Ordinal just save the numeric values for all the enums and String save the respecting string values.<br>
    It is good idea to use String since, if we need to introduce any new type in future, the numeric sequence will go haywire. 