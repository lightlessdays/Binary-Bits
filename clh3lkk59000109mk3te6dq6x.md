---
title: "Data Models in DBMS"
datePublished: Sun Apr 30 2023 15:59:35 GMT+0000 (Coordinated Universal Time)
cuid: clh3lkk59000109mk3te6dq6x
slug: data-models-in-dbms
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682870349250/cf3026d6-bbe2-4421-a8b2-d3acb0563010.png
tags: dbms

---

Nowadays, all enterprises require properly defined and formatted data to bring all the segments of an enterprise - IT, Management, and others together. Data models play a key role in solving this problem as they represent an enterprise's data and connections between them in a pictorial form. Data models in DBMS help to understand the design at the conceptual, physical, and logical levels as it provides a clear picture of the data making it easier for developers to create a physical database.

Data models are used to describe how the data is stored, accessed, and updated in a DBMS. A set of symbols and text is used to represent them so that all the members of an organization can understand how the data is organized. It provides a set of conceptual tools that are vastly used to represent the description of data. This article is part of a series on DBMS. Check out the complete series here: [**https://binarybits.hashnode.dev/series/dbms**](https://binarybits.hashnode.dev/series/dbms)**.**

Many types of data models are used in the industry. We are going to look at all of them one by one.

### Hierarchical Model

The hierarchical data model is one of the oldest data models, developed in the 1950s by IBM. In this data model, the data is organized in a hierarchical tree-like structure. This data model can be easily visualized because each record in DBMS has one parent and many children (possibly none) as shown in the image given below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682869632688/36aa17e3-9792-47d9-9a3b-5d6b40012dd5.png align="center")

The above-given image represents the data model of the Vehicle database, Vehicles are classified into two types Viz. two-wheelers and four-wheelers and then they are further classified.

The main drawback we can see here is we can only have one too many relationships under this model, hence the hierarchical data model is very rarely used nowadays.

### Network Model

A network model is nothing but a generalization of the hierarchical data model as this data model allows many to many relationships therefore in this model a record can also have more than one parent.

The network model in DBMS can be represented as a graph and hence it replaces the hierarchical tree with a graph in which object types are the nodes and relationships are the edges.

For example:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682869785671/263ced2b-6676-4967-9c02-3b31cc131a2d.png align="center")

Here you can see all three departments are linked with the director which was not possible in the hierarchical data model.

In the network model, there can be many possible paths to reach a node from the root node (College is the root node in the above case), therefore the data can be accessed efficiently when compared to the hierarchical data model. But, on the other hand, the process of insertion and deletion of data is quite complex.

### Entity Relationship (E-R) Model

An Entity-Relationship model is a high-level data model that describes the structure of the database in a pictorial form which is known as an ER diagram. In simple words, an ER diagram is used to represent the logical structure of the database easily.

ER model develops a conceptual view of the data hence it can be used as a blueprint to implement the database in the future. Developers can easily understand the system just by looking at ER diagram. Let's first have a look at the components of an ER diagram.

**Entity-** Anything that has an independent existence about which we collect the data. To learn more about Entity in DBMS click here. They are represented as rectangles in the ER diagram. For example - Car, house, and employee.

**Entity Set-** A set of the same type of entities is known as an entity set. For example - A set of students studying in a college. Attributes - Properties that define entities are called attributes. They are represented by an ellipse shape. Relationships - A relationship in DBMS is used to describe the association between entities. They are represented as diamond or rhombus shapes in the ER diagram.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682869962100/1b3ea107-dc98-4281-8252-91e6d3934408.png align="center")

In the above-represented ER diagram, we have two entities that are Employee and Company, and the relationship among them. Also, in the above-represented ER diagram, we can see that both the employee and company have some attributes and the relationship is of "works in" type, which means the employee works in a company.

### Relational Model

This is the most widely accepted data model. In this model, the database is represented as a collection of relations in the form of rows and columns of a two-dimensional table. Each row is known as a tuple (a tuple contains all the data for an individual record) while each column represents an attribute. For example:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682870168405/eab2740e-cebf-40ab-b1b6-a0eac3e4d94d.png align="center")

The above table shows a relation "STUDENT" with attributes such as Stu. Id, Name, and Branch which consists of 4 records or tuples.

There are several other kinds of data models as well, but we are not concerned with them right now. We only wanted a gist of some data models.

Let us look at the Advantages and Disadvantages of Data Models in DBMS.

### Advantages of Data Models

The following are the advantages of data models:

* Data models ensure that the data is represented accurately.
    
* The relationship between the data is well-defined.
    
* Data Redundancy in DBMS can be minimized and missing data can be identified easily.
    
* Last but not least, the security of the data is not compromised.
    

### Disadvantages of Data Models

The following are the disadvantages of data models:

* The biggest disadvantage of the data model is, one must know the characteristics of physical data to build a data model.
    
* Sometimes in big databases, it is quite difficult to understand the data model also the cost incurred is very high.