# How React Works Under the Hood

## Introduction

In this document, we will explore the inner workings of React.

## Table of Contents
1. [Regular DOM](#regular-dom)
2. [Virtual DOM](#virtual-dom)
3. [Reconciliation](#reconciliation)

## Regular DOM
The Regular DOM is often slow because it directly updates the entire tree structure, leading to performance bottlenecks, especially with complex and large documents. Each change in the DOM can cause the browser to re-render the entire page, which is resource-intensive.

### Key Points:
- **Tree Structure**: The DOM represents the document as a tree with parent, child, and sibling relationships.
- **Nodes**: Every part of the document (elements, attributes, text) is a node.
- **Interactivity**: Scripts can interact with the DOM to create dynamic and interactive web experiences.
- **Performance**: Direct updates to the DOM can be slow and inefficient, causing performance issues in complex applications.

### Exemple

```html
<!DOCTYPE html>
<html>
  <head>
    <title>DOM Example</title>
  </head>
  <body>
    <h1 id="main-heading">Hello, World!</h1>
    <p class="intro">Welcome to the DOM tutorial.</p>
    <button id="change-text">Change Text</button>
  </body>
</html>
```

```bash
Document
└── html
    ├── head
    │   └── title
    │       └── "DOM Example"
    └── body
        ├── h1#main-heading
        │   └── "Hello, World!"
        ├── p.intro
        │   └── "Welcome to the DOM tutorial."
        └── button#change-text
            └── "Change Text"

```


## Virtual DOM

In react there is a virtual DOM. The virtual DOM is managed by react and is a more reliable and efficient js structure.


## Reconciliation