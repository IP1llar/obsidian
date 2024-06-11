## Aims

This course introduces basic concepts for database systems as seen from the perspective of application designers. That is, the focus is on the abstractions supported by database management systems and not on how those abstractions are implemented.

The database world is currently undergoing swift and dramatic transformations largely driven by Internet-oriented applications and services. Today many more options are available to database application developers than in the past and so it is becoming increasingly difficult to sort fact from fiction. The course attempts to cut through the fog with a practical approach that emphasises engineering tradeoffs that underpin these recent developments and also guide our selection of “the right tool for the job.”

This course covers three approaches. First, the traditional mainstay of the database industry -- the relational approach -- is described with emphasis on eliminating logical redundancy in data. Then two representatives of recent trends are presented -- graph-oriented and document-oriented databases. The lectures are supported with two Help and Tick sessions, where students gain hands-on experience and guidance with the Assessed Exercises (ticks).

## Lectures

- L1 **Introduction**. What is a database system? What is a data model? Typical DBMS configurations and variations (fast queries or reliable update). In-core, in secondary store or distributed.
- L2 **Conceptual modelling**. Entities, relations, E/R diagrams and implementation-independent modelling, weak entities, cardinality.
- L3+4 **The relational database model**. Implementing E/R models with relational tables. Relational algebra and SQL. Basic query primitives. Update anomalies caused by redundancy. Minimising redundancy with normalised schemas.
- L5 **Transactions**. On-Line Transaction Processing. On-line Analytical Processing. Reliability, throughput, normal forms, ACID, BASE, eventual consistency.
- L6 **Documents and semi-structured data**. The NoSQL, schema-free movement. XML/JSON. Key/value stores. Embracing data redundancy: representing data for fast, application-specific access. Path queries (if time permits).
- L7 **Further SQL**. Multisets, NULL values, aggregates, transitive closure, expressibility (nested queries and recursive SQL).
- L8 **Graph databases**. Optimised for processing enormous numbers of nodes and edges. Implementing E/R models in a graph-oriented database. Comparison of the presented models.

## Objectives

At the end of the course students should

- be able to design entity-relationship diagrams to represent simple database application scenarios
- know how to convert entity-relationship diagrams to relational- and graph-oriented implementations
- understand the fundamental tradeoff between the ease of updating data and the response time of complex queries
- understand that no single data architecture can be used to meet all data management requirements
- be familiar with recent trends in the database area.

Textbook relevant pages:
1. What is a Database Management System (DBMS)? 
	- Chapter 2 
2. Entity-Relationship (ER) diagrams 
	- Sections 3.1 and 3.2
3. Relational Databases ... 
	- Sections 6.1, 6.2.1, 6.2.2, and 6.3
4. ... and SQL 
	- Sections 7.2 – 7.4 5 
5. Indexes. Some limitations of SQL ... 
	- 7.5, 
6. ... that can be solved with Graph Database 
	- Sections 11.1 and 11.5 
7. Document-oriented Database
	- Chapter 10 and Section 11.3

- Lecture Notes [PDF](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/databases_2324_1to8-D.pdf). Erratum: I have now removed the 'non-examinable' remark from the slide about transaction abort because it is implementation details that are in Ib, not the concept.
    
- James Sharkey has written three tutorials for you to follow and learn in your own time (especially the first one):
    
    2. Relational DBMS Tutorial [HERE](https://www.cl.cam.ac.uk/teaching/2324/Databases/relational.html).
        
    3. Document DBMS Tutorial [HERE](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/document.html).
        
    4. Graph DBMS Tutorial [HERE](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/graph-highlighted.html).
    
    Many thanks to James Sharkey of the Computer Lab for preparing the tutorials this year.
    
    -- As well as everything in the lecture notes (unless specifically marked non-examinable), you are expected to thoroughly know the contents of the Relational Tutorial for Tripos examination purposes in Summer 2024.  
    -- You will need knowledge from the Relational and Document Tutorials to complete the two Assessed Exercises.  
    -- Understanding the principle differences between the three forms is part of the course syllabus and so Tripos questions will lightly touch on the contents of the Document and Graph Tutorials.

## Supervision Materials

- Supervision 1: [Kick-off Supervision Materials](https://www.cl.cam.ac.uk/teaching/2223/Databases/wide-range-and-tripos-1977/wide-range.html) and the [Main Supervision Sheet 1](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/supervision-1.html).
    
- Supervision 2: [Main Supervision Sheet 2](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/supervision-2.html).
    
- Supervision 3: [Main Supervision Sheet 3](https://www.cl.cam.ac.uk/teaching/2324/Databases/djg-materials/supervision-3.html).

## Secondary Materials

- Interesting 'The Register' article: September 2023: [MongoDB's SQL-to-NoSQL converter uses AI to smash the language barrier](https://www.theregister.com/2023/09/27/mongodb_automated_sql_converter/?td=keepreading "undefined (Link to an external website)")
    
- A book on graph algorithms using Neo4j: [Graph Algorithms (full text, PDF)](https://www.cl.cam.ac.uk/teaching/2122/Databases/Neo4j_Graph_Algorithms.pdf) note: most of the content relates to the Ia Algorithms course, rather than this course.