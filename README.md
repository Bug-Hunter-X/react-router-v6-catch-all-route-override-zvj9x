# React Router v6 Catch-All Route Issue

This repository demonstrates a subtle issue in React Router v6 related to the catch-all route (`path="/*"`). When a catch-all route is defined, even after more specific routes, it will always match first, overriding other, more specific paths.

## Problem Description:
The `path="/*"` route in the example will always be matched, even if a different route matches first. This means that, even when you navigate to `/about`, it'll render the NotFound component instead of the About component.

## Solution:
The correct approach is to place the catch-all route at the end of your route definitions, to allow more specific routes to be matched first.  Order matters!