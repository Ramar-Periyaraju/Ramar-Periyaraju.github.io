---
title: About Pega Constellation Architecture
date: 2024-06-20 20:11 +0300
categories: [Pega, UI]
tags: [Pega, Pega Constellation, Architecture, UI]
author: Ramar Periyaraju
---

### Overview

The architecture diagram illustrates how the Constellation UX framework integrates with both the Pega system and an alternate design system, showing the different layers and components involved in delivering the user interface and user experience.

![Desktop View](/assets/img/ConstellationDiagram.png)

### Key Components

1. **Device**

   - Represents the user’s device (e.g., browser, mobile app) where the user interface is rendered.

2. **Constellation Design System (Pega's Front End)**

   - **Constellation Presentational Components**: UI components responsible for displaying the user interface elements.
   - **Constellation DX Components**: Digital Experience components that handle interactions and data exchange with the backend.
   - **Customer Extension: DX Components**: Customizable components that allow for customer-specific extensions within the Constellation DX framework.

3. **Alternate Design System (Your Front End)**

   - **Alternate Design System Presentational Components**: UI components that follow a different design system but serve the same purpose of displaying UI elements.
   - **Alternate Design System DX Components**: Digital Experience components specific to the alternate design system, handling interactions and data exchange.

4. **Constellation Orchestration Layer (Public API)**

   - Acts as an intermediary layer that orchestrates interactions between the design system components and the Pega Infinity Server. It exposes a public API that can be utilized by both Constellation and alternate design systems.

5. **Pega Infinity Server**
   - The backend system where core business logic, data processing, and server-side operations take place. It interacts with the Constellation Orchestration Layer via the Constellation DX API.

### Interaction Flow

1. **User Interaction**:

   - Users interact with the UI rendered on their devices, which could be built using either the Constellation Design System or an Alternate Design System.

2. **Presentation Layer**:

   - The presentational components from the chosen design system display the necessary UI elements.

3. **DX Components**:

   - These components handle user interactions, gather data, and communicate with the backend through the orchestration layer.

4. **Orchestration Layer**:

   - This layer manages the communication between the frontend components and the backend Pega Infinity Server. It ensures that API calls are correctly routed and processed.

5. **Backend Operations**:

   - The Pega Infinity Server processes the requests, performs necessary business logic, and returns responses back through the orchestration layer to the DX components.

6. **Rendering Response**:
   - The DX components update the presentational components with the received data, and the UI is updated on the user’s device accordingly.

### Color Coding

- **Blue Components**: Represent Pega’s Constellation Design System and related orchestration components.
- **Orange Components**: Represent the customer’s or an alternate front-end design system that can integrate with Pega’s backend via the same orchestration layer.

This architecture allows for flexibility in choosing or extending the front-end design system while ensuring robust integration with Pega’s backend services through a standardized API layer.
