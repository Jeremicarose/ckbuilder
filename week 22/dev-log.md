# Builder Track Weekly Report — Week 22
**Name:** Jeremic  
**Week Ending:** 10 August

## Overview

This week focused on reviewing and improving the **MLAT Airspace Console frontend**. The main finding was that the application was too page-oriented and felt more like a technical report than an interactive operational console.

## Completed Work

### Frontend UX Review

Reviewed the major application areas:

- Overview
- Live Map
- Aircraft
- Receivers
- Pipeline
- Metrics
- Environment
- Settings

Identified key issues including excessive scrolling, weak interaction between pages, static information displays, and limited operator guidance.

### New UX Direction

Defined a new **investigation-based interface** where all pages share the same operational state.

The new approach will include:

- Live Map as the primary interaction surface
- Persistent aircraft/receiver inspector
- Shared selection across pages
- Interactive timeline and replay
- Synchronized maps, charts, metrics, and evidence
- Reduced scrolling and navigation
- More contextual actions and progressive information disclosure

### Frontend Redesign Plan

The redesign was organized into five phases:

1. Rebuild the application shell and global interaction model.
2. Make Live Map the primary interaction engine.
3. Rebuild Overview, Aircraft, and Receivers around investigation workflows.
4. Rebuild Pipeline, Metrics, and Environment as specialized workspaces.
5. Add motion, keyboard navigation, saved investigations, and final UX polish.

## Current Status

The backend and CKB infrastructure remain operational, while the frontend is now the main area being improved.

The target is to transform the application from a collection of dashboard pages into a **smooth, interactive airspace operations console**.

## Next Steps

- Implement the new application shell.
- Introduce persistent inspectors and timeline.
- Synchronize map, aircraft, receivers, metrics, and evidence.
- Reduce unnecessary scrolling.
- Validate the redesigned interface using real operator workflows.
- drafting grant proposal

## Summary

Week 22 established a major UX direction for the project:

