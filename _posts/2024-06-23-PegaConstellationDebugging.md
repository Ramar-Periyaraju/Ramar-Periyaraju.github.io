---
title: Pega Constellation Debugging Tools
date: 2024-06-27 22:00 +0300
categories: [Pega, Constellation]
tags: [Pega, Debugging, Constellation]
author: Ramar Periyaraju
---

## Introduction

Debugging Constellation applications requires a different approach compared to traditional Pega applications due to their stateless nature. This article explores the various tools available for debugging Pega Constellation applications.

## Key Debugging Tools

### 1. Browser DevTools

Browser DevTools are essential for debugging Constellation applications[4]:

- **Console tab**: Displays working scripts on the web page.
- **Network tab**: Shows DX API calls (filter by Fetch/XHR).
- **Application tab**: Allows inspection of items cached in Local and Session storage.

To access DevTools in Chrome, Firefox, or Edge, press F12[4].

### 2. Tracer Tool

The Tracer tool is still supported for Constellation applications with some changes[2]:

- Output is grouped by Constellation DX API call.
- Each UI action generates a separate DX API call.
- New "View Rules" setting enables tracing Views and investigating View metadata[2].

### 3. DebugPegaAPI Dynamic System Setting

Set the DebugPegaAPI dynamic system setting to true for more verbose debugging of API calls[2]. This logs additional fields in Pega API Rest Service Info statements, helping debug Page instructions and field-level security[2].

### 4. View Debugging in Dev Studio

Access View metadata in Dev Studio by setting the `pxEnableC11nDev` When Rule to true[2]. This allows you to inspect the JSON associated with individual Views.

### 5. PCore and PConnect APIs

These APIs provide debugging capabilities for client-side operations[4]:

- `PCore.getDataPageUtils()`: Logs information about client-side cached Data Pages[4].
- `PCore.getDebugger().toggleXRay(true/false)`: Enables/disables X-Ray visualization of UI components[4].

### 6. React and Redux DevTools

Browser extensions for debugging React applications:

- **React DevTools**: Inspect React component hierarchies.
- **Redux DevTools**: Visualize state modifications and inspect state and action payloads[4].

## Limitations

- The Pega Clipboard is only partially supported and usable only for investigating static data in Preview mode[2].
- LiveUI is not supported for debugging Constellation applications[2].

## Best Practices

1. Use the Tracer tool for backend debugging and API call analysis.
2. Leverage browser DevTools for frontend and network debugging.
3. Utilize PCore and PConnect APIs for client-side debugging.
4. Enable DebugPegaAPI for detailed API error logging.
5. Use React and Redux DevTools for component and state debugging.

## Conclusion

Debugging Constellation applications requires a combination of traditional Pega tools and modern web development tools. By mastering these tools, developers can effectively troubleshoot and optimize their Constellation applications.

## References

1. Pega Academy: [Tools for debugging Constellation applications](https://academy.pega.com/module/tools-debugging-constellation-applications/v1)
2. Pega Academy: [Pega tools for debugging Constellation applications](https://academy.pega.com/topic/pega-tools-debugging-constellation-applications/v1)
3. Pega Academy: [Debugging Constellation applications](https://academy.pega.com/challenge/debugging-constellation-applications/v1)
4. Pega Academy: [Examining Constellation using DevTools](https://academy.pega.com/topic/examining-constellation-using-devtools/v1)
