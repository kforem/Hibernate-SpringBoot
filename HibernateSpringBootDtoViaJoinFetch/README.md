**[How To Avoid LazyInitializationException Via JOIN FETCH](https://github.com/AnghelLeonard/Hibernate-SpringBoot/tree/master/HibernateSpringBootJoinFetch)**

**Description:** Typically, when we get a `LazyInitializationException` we tend to modify the relationship fetching type from `LAZY` to `EAGER`. That is bad! This is a [code smell](https://vladmihalcea.com/eager-fetching-is-a-code-smell/). Best way to avoid this exception is to rely on `JOIN FETCH` + DTOs (if needed). This application is a `JOIN FETCH` example with no DTOs. But, based on the DTOs examples from this repo, you can easily adapt it to use DTOs as well.

**Key points:**\
     - define two related entities (e.g., `Author` and `Book` in a one-to-many lazy bidirectional relationship)\
     - write a JPQL `JOIN FETCH` to fetch an author including his books\
     - write a JPQL `JOIN FETCH` to fetch a book including its author

**Output example:**\
![](https://github.com/AnghelLeonard/Hibernate-SpringBoot/blob/master/HibernateSpringBootJoinFetch/hibernate%20spring%20boot%20join%20fetch.png) 

<a href="https://leanpub.com/java-persistence-performance-illustrated-guide"><p align="center"><img src="https://github.com/AnghelLeonard/Hibernate-SpringBoot/blob/master/Java%20Persistence%20Performance%20Illustrated%20Guide.jpg" height="410" width="350"/></p></a>