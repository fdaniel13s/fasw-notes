# C4 Model - All you need to know - by [Fernando Quispe](https://linkdln.com/in/fernando-quispe)

## ¿What is C4 Model?

The C4 model is an "abstraction-first" approach to diagramming software architecture, based upon abstractions that reflect how software architects and developers think about and build software. The small set of abstractions and diagram types makes the C4 model easy to learn and use.

## ¿Why you should use C4 Model?

The C4 model is a way to create a set of maps that describe the architecture of a software system. The C4 model was created as a way to help software development teams describe and communicate software architecture, both during up-front design sessions and when retrospectively documenting an existing codebase. For example, the C4 model can be used to describe the static structure of a system in terms of containers, components, and code classes, and to describe the dynamic behavior of a system in terms of collaborations between components and code classes.

## ¿What is the difference between C4 Model and any other diagram representing software architecture?

- C4 Model is an "abstraction-first" approach to diagramming software architecture.
- Have consistent notation(colour coding, shapes, line styles, etc)
- Don't have ambigous names
- Don't have unlabelled relationships
- The terminilogy is consistent
- The technology is present but not the focus

## Key Concepts

- C4 Model can be used in two fronts, during up-front design sessions and when retrospectively documenting an existing codebase.
- Have various levels of detail, from a high-level overview down to the code level.
- A **System Context** diagram provides a starting point, showing how the software system in scope fits into the world around it.
- A **Container diagram** zooms into the software system in scope, showing the high-level technical building blocks.
- A **Component diagram** zooms into an individual container, showing the components inside it. Like
individual container it is possible have more than one component diagram.
- A **Code diagram** can be used to zoom into an individual component, showing how that component is implemented.
- It is important that you know that is not necessary to create all the diagrams, you can create only the necessary ones.

## Concepts

- Person: A person represents one of the human users of your software system (e.g. actors, roles, personas, etc).
- Software System: A software system is the highest level of abstraction and describes something that delivers value to its users, whether they are human or not.This includes the software system you are modelling, and the other software systems upon which your software system depends.
- Container: Represents an application or a data store. A container is something that needs to be running in order for the overall software system to work. Examples of containers include server-side web applications, mobile apps, desktop applications, databases, file systems, message queues, etc.
- Component: In C4 Model, is grouping of related functionality encapsulated behind a well-defined interface. In this context, components are not separately deployable units.

## Diagrams

### System Context Diagram

Detail isn't important here as this is your zoomed out view showing a big picture of the system landscape. The focus should be on people (actors, roles, personas, etc) and software systems rather than technologies, protocols and other low-level details.

### Container Diagram

Shows the high-level shape of the software architecture and how responsibilities are distributed across it. It also shows the major technology choices and how the containers communicate with one another. It's a simple, high-level technology focussed diagram that is useful for software developers and support/operations staff alike.

### Component Diagram

The Component diagram shows how a container is made up of a number of "components", what each of those components are, their responsibilities and the technology/implementation details. It can be connected with
containers, people, and other software.

### Code Diagram

The Code diagram shows how a component is implemented. It shows the structure of the codebase and dependencies between classes, interfaces, and other code elements.

## Bibliography

- [C4 Model by Simon Brown](https://c4model.com/)