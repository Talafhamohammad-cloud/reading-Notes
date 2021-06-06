## What is a component?

### A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.
### A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

## What are the charactistics of a component?

### Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.
### Replaceable − Components may be freely substituted with other similar components.
### Not context specific − Components are designed to operate in different environments and contexts.
### Extensible − A component can be extended from existing components to provide new behavior.
### Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.
### Independent − Components are designed to have minimal dependencies on other components.

## What are the advantages of using component based architecture?

**Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties.**
**advantages of using component based architecture is that It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions.**

***Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.***
***Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.***
***Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.***
***Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.***
***Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.***
***Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.***
***System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.***
***Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.***



## What is props short for?

React is a component-based library which divides the UI into little reusable pieces. those components communicate (send data to each other) by using props(keyword in React, which stands for properties)


1-props used for passing data from one component to another uni-directional flow (one way from parent to child)

2-props data is immutable (read-only) (data coming from the parent should not be changed by child components.)

3-Prop is an Object

## How are props used in React?

define an attribute and its value(data) Then pass it to child component(s) by using Props

## What is the flow of props?

uni-directional flow, only be passed to components in one-way (parent to child)