---
title: API Training
author: Adi Iyengar
patat:
    incrementalLists: true
    theme:
        emph: [vividWhite, onVividBlack, bold]
        imageTarget: [onDullWhite, vividGreen]
    pandocExtensions:
      - patat_extensions
      - autolink_bare_uris
      - emoji
...

# MAIN

```
 █████╗ ██████╗ ██╗███████╗     █████╗ ███╗   ██╗██████╗     ███████╗███╗   ███╗███████╗    ███████╗███╗   ██╗ ██████╗ ██╗███╗   ██╗███████╗
██╔══██╗██╔══██╗██║██╔════╝    ██╔══██╗████╗  ██║██╔══██╗    ██╔════╝████╗ ████║██╔════╝    ██╔════╝████╗  ██║██╔════╝ ██║████╗  ██║██╔════╝
███████║██████╔╝██║███████╗    ███████║██╔██╗ ██║██║  ██║    █████╗  ██╔████╔██║███████╗    █████╗  ██╔██╗ ██║██║  ███╗██║██╔██╗ ██║█████╗
██╔══██║██╔═══╝ ██║╚════██║    ██╔══██║██║╚██╗██║██║  ██║    ██╔══╝  ██║╚██╔╝██║╚════██║    ██╔══╝  ██║╚██╗██║██║   ██║██║██║╚██╗██║██╔══╝
██║  ██║██║     ██║███████║    ██║  ██║██║ ╚████║██████╔╝    ██║     ██║ ╚═╝ ██║███████║    ███████╗██║ ╚████║╚██████╔╝██║██║ ╚████║███████╗
╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝    ╚═╝  ╚═╝╚═╝  ╚═══╝╚═════╝     ╚═╝     ╚═╝     ╚═╝╚══════╝    ╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝╚═╝  ╚═══╝╚══════╝

```

# HELPFUL RESOURCES

API: Design Matters (_https://queue.acm.org/detail.cfm?id=1255422_)
Inversion of Control (_https://martinfowler.com/bliki/InversionOfControl.html_)


# TOPICS

- Basics of APIs
- Web APIs
- Enterprise Software Communication
- RESTful Web APIs with Rails
- FMS Engine


---
# notes

---

---
# questions/notes while presenting

---


# APIs

- What are APIs?
- _Application Programming Interface_:
Set of tools or protocols to interact with an application.

- Why use APIs?
- APIs make it easier for developers to use certain tools while writing an application, without
having to worry about the business logic of the tool.

- Examples of APIs
- Ruby API, SQL, Operating System tools, pokeAPI


---
# notes

- APIs could be for a web-based system, a software library, a database, OS etc
- It is a set of methods of communication between various software components

---

---
# questions/notes while presenting

---


# API style Design

- APIs just describe the _expected behaviour_ of an application while hiding
the actual implementation of that behaviour.

- Promotes Inversion of Control
- __Inversion of Control__:
Design where the flow of control is dictated by the software and not by the
caller in contrast to traditional procedural programming.


---
# notes

- The separation of behaviour from implementation allows cross platform usage,
more modular design (DDD, Inversion of Control) and better information hiding.

- Inversion of Control allows developers to:
decouple the execution of a task from implementation.
focus a module on the task it is designed for.
free modules from assumptions about how other systems do what they do and instead rely on contracts.
prevent side effects when replacing a module.

---

---
# questions/notes while presenting

---


# Web APIs (Server Side)

- An API for a web server.
- Consists of one or more exposed endpoints.
- Has a defined protocol for a request-response cycle, typically in JSON or XML,
usually through HTTP.
- API types: SOAP, REST, XML, GraphQL
- Rails natively supports REST.
- We use REST in FMS.


---
# notes

- REST is a stateless protocol.

- REST-compliant Web services allow requesting systems to access and manipulate
textual representations of Web resources using a uniform and predefined set of
stateless operations

- REST is used because of simplicity, reliability, scalability and performance

---

---
# questions/notes while presenting

---


# Emterprise Software Communication

- __Loosely-coupled system__:
A system where each _component_ has no knowledge of implementations of other
componenets. (API-based interaction)

- __Service-Oriented Architecture vs Feeds__ --> _Integrity vs Availability_


---
# notes

---

---
# questions/notes while presenting

---


# RESTful API in Rails

- Rails >= 5.0 have native support for server-side API.
- For client-side, we use `faraday` and `her` gems.
- Store App:
      - products (& categories)
      - api endpoint for products
      - api client the consumes that endpoint

# -----------------

```
██╗     ███████╗████████╗███████╗     ██████╗ ██████╗ ██████╗ ███████╗██╗
██║     ██╔════╝╚══██╔══╝██╔════╝    ██╔════╝██╔═══██╗██╔══██╗██╔════╝██║
██║     █████╗     ██║   ███████╗    ██║     ██║   ██║██║  ██║█████╗  ██║
██║     ██╔══╝     ██║   ╚════██║    ██║     ██║   ██║██║  ██║██╔══╝  ╚═╝
███████╗███████╗   ██║   ███████║    ╚██████╗╚██████╔╝██████╔╝███████╗██╗
╚══════╝╚══════╝   ╚═╝   ╚══════╝     ╚═════╝ ╚═════╝ ╚═════╝ ╚══════╝╚═╝
```



