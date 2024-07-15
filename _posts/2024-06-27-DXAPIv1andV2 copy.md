---
title: Constellation Runtime Architecture & Its Components.
date: 2024-06-27 21:00 +0300
categories: [Pega, Constellation]
tags: [Pega, DX API, Constellation]
author: Ramar Periyaraju
---

# Constellation Runtime Architecture

The Constellation Runtime architecture consists of two main parts:

- server-side components built in Pega Infinity
- client-side components

## 1. Server-side: Pega Infinity Platform

- This is where the Constellation Digital Experience (DX) API is implemented.
- For Pega Constellation, DX API Version 2 is used.
- DX API V2 is a RESTful API that provides both UI metadata and contextual data in a single response.

## 2. Client-side Components

### a. Constellation JS Engine and Public JS APIs (PCore and PConnect)

- The Constellation JS Engine is responsible for overall runtime UI orchestration.
- It's built using ES6 (ECMAScript 2015) and is framework-agnostic, supporting React, Angular, and Web Components.
- Key components include:
  - Bootstrap for application initialization
  - Environment Info for runtime configuration
  - Asset Loader for managing scripts, styles, and images
  - Rest Client for HTTP requests
  - State Manager (Redux) for application state management
  - PubSub and Messaging Service for component communication
  - CRUD Manager for data operations
  - Component Manager for UI component management
  - Public JS APIs include features like Promises for async operations, Mashup Bridge, and various processors (Property, Expression, When, Localization).

### b. Constellation Front End React Bridge

- This bridge connects the Constellation JS Engine with the presentation layer.
- It includes Constellation DX components provided by Pega, available on GitHub (Constellation UI gallery).
- It also supports custom DX components for extending functionality (Web Component Builder).

### c. Presentation Component

- Available at [design.pega.com](https://design.pega.com)
- Manages the user interface and interactions.

## 3. DX API V2

- Provides both UI metadata and contextual data in a single response.
- The primary consumer of the DX API is the Constellation JS Engine.

## 4. Additional Components

- **Service Broker:** Acts as an intermediary connecting various services.
- **Constellation Messaging Server:** Manages messaging services and includes Web Sockets for real-time communication.

This architecture follows modern design paradigms such as stateless architecture, client orchestration, and modular design. It allows for a more streamlined, manageable, and efficient system compared to traditional architectures. The Constellation architecture's modular and flexible design enables it to support a wide variety of network types, devices, and environments while reducing design and installation resources and time.

### Pega Site References

1. [Characteristics of Constellation Architecture](https://support.pega.com/discussion/characteristics-constellation-architecture)
2. [Anatomy of Constellation UI](https://academy.pega.com/topic/anatomy-constellation-ui/v1)
3. [Constellation Architecture](https://academy.pega.com/topic/constellation-architecture/v1)
4. [Build Constellation DX Components](https://community.pega.com/video-library/build-constellation-dx-components)
