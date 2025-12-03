---
title: The Post class
---
# Intro

This document will cover the class Post in the codebase. We will cover:

1. What is Post
2. Variables and functions of Post

# What is Post

Post is a class defined in the file <SwmPath>[models/post.asp](models/post.asp)</SwmPath>. It represents a data model for a post entity, typically used to encapsulate the properties of a post such as its identifier, title, content, and status. This class provides a structured way to manage post data within the application.

<SwmSnippet path="/models/post.asp" line="4">

---

The variable <SwmToken path="models/post.asp" pos="4:3:3" line-data="    Private p_seq">`p_seq`</SwmToken> is a private class member used to store the unique sequence identifier of a Post instance. It is accessed and modified through public property methods.

```asp
    Private p_seq
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="5">

---

The variable <SwmToken path="models/post.asp" pos="5:3:3" line-data="    Private p_title">`p_title`</SwmToken> is a private class member used to store the title of the Post. It is encapsulated and accessed via getter and setter properties.

```asp
    Private p_title
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="6">

---

The variable <SwmToken path="models/post.asp" pos="6:3:3" line-data="    Private p_content">`p_content`</SwmToken> is a private class member that holds the content body of the Post. It is accessed and modified through public property methods.

```asp
    Private p_content
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="7">

---

The variable <SwmToken path="models/post.asp" pos="7:3:3" line-data="    Private p_status">`p_status`</SwmToken> is a private class member representing the status of the Post, such as published or draft. It is encapsulated with getter and setter properties.

```asp
    Private p_status
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="10">

---

The function <SwmToken path="models/post.asp" pos="10:7:7" line-data="    Public Property Get Seq()">`Seq`</SwmToken> is a public getter property that returns the value of the private variable <SwmToken path="models/post.asp" pos="11:5:5" line-data="      Seq = p_seq">`p_seq`</SwmToken>. It allows external code to read the sequence identifier of the Post.

```asp
    Public Property Get Seq()
      Seq = p_seq
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="13">

---

The function <SwmToken path="models/post.asp" pos="13:7:7" line-data="    Public Property Let Seq(value)">`Seq`</SwmToken> is also a public setter property that assigns a value to the private variable <SwmToken path="models/post.asp" pos="14:1:1" line-data="      p_seq = value">`p_seq`</SwmToken>. It allows external code to set the sequence identifier of the Post.

```asp
    Public Property Let Seq(value)
      p_seq = value
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="17">

---

The function <SwmToken path="models/post.asp" pos="17:7:7" line-data="    Public Property Get Title()">`Title`</SwmToken> is a public getter property that returns the value of the private variable <SwmToken path="models/post.asp" pos="18:5:5" line-data="      Title = p_title">`p_title`</SwmToken>. It allows external code to read the title of the Post.

```asp
    Public Property Get Title()
      Title = p_title
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="20">

---

The function <SwmToken path="models/post.asp" pos="20:7:7" line-data="    Public Property Let Title(value)">`Title`</SwmToken> is also a public setter property that assigns a value to the private variable <SwmToken path="models/post.asp" pos="21:1:1" line-data="      p_title = value">`p_title`</SwmToken>. It allows external code to set the title of the Post.

```asp
    Public Property Let Title(value)
      p_title = value
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="24">

---

The function <SwmToken path="models/post.asp" pos="24:7:7" line-data="    Public Property Get Content()">`Content`</SwmToken> is a public getter property that returns the value of the private variable <SwmToken path="models/post.asp" pos="25:5:5" line-data="      Content = p_content">`p_content`</SwmToken>. It allows external code to read the content of the Post.

```asp
    Public Property Get Content()
      Content = p_content
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="27">

---

The function <SwmToken path="models/post.asp" pos="27:7:7" line-data="    Public Property Let Content(value)">`Content`</SwmToken> is also a public setter property that assigns a value to the private variable <SwmToken path="models/post.asp" pos="28:1:1" line-data="      p_content = value">`p_content`</SwmToken>. It allows external code to set the content of the Post.

```asp
    Public Property Let Content(value)
      p_content = value
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="31">

---

The function <SwmToken path="models/post.asp" pos="31:7:7" line-data="    Public Property Get Status()">`Status`</SwmToken> is a public getter property that returns the value of the private variable <SwmToken path="models/post.asp" pos="32:5:5" line-data="      Status = p_status">`p_status`</SwmToken>. It allows external code to read the status of the Post.

```asp
    Public Property Get Status()
      Status = p_status
    End Property
```

---

</SwmSnippet>

<SwmSnippet path="/models/post.asp" line="34">

---

The function <SwmToken path="models/post.asp" pos="34:7:7" line-data="    Public Property Let Status(value)">`Status`</SwmToken> is also a public setter property that assigns a value to the private variable <SwmToken path="models/post.asp" pos="35:1:1" line-data="      p_status = value">`p_status`</SwmToken>. It allows external code to set the status of the Post.

```asp
    Public Property Let Status(value)
      p_status = value
    End Property
```

---

</SwmSnippet>

# Usage

## Usage in <SwmPath>[database-write.asp](database-write.asp)</SwmPath>

In <SwmPath>[database-write.asp](database-write.asp)</SwmPath>, the Post class is instantiated repeatedly within a loop that iterates over database records. Each Post object is populated with the title, content, and status fields from the current record. This allows the application to represent each database entry as a Post object for further processing or display.

## Usage in <SwmPath>[database-update.asp](database-update.asp)</SwmPath>

In <SwmPath>[database-update.asp](database-update.asp)</SwmPath>, the Post class is used in multiple ways. Initially, a new Post object is created and assigned values from form inputs to prepare for updating a post. Later, the class is used to load a single post from the database by querying with a sequence identifier and populating a Post object with the retrieved data. Additionally, the class is used to create lists of Post objects from database queries filtering posts by deletion status, enabling the application to manage and display posts based on whether they are marked as deleted or not.

## Usage in Forms

Both <SwmPath>[database-write.asp](database-write.asp)</SwmPath> and <SwmPath>[database-update.asp](database-update.asp)</SwmPath> include HTML forms for creating and updating posts, respectively. These forms collect user input such as the post's title and content, which are then assigned to Post objects in the server-side code. This integration between form data and Post objects facilitates the creation and modification of posts in the database.

&nbsp;

*This is an auto-generated document by Swimm 🌊 and has not yet been verified by a human*

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBbGVhcm4tY2xhc3NpYy1hc3AlM0ElM0FtdWRhc2luMQ==" repo-name="learn-classic-asp"><sup>Powered by [Swimm](https://app.swimm.io/)</sup></SwmMeta>
