# Challenge: Build a Simple PHP Router

## Difficulty
Medium

## Description
Create a lightweight URL router in PHP that maps incoming request URLs to corresponding controller functions without using any external frameworks. The router should support static routes, dynamic parameters, and HTTP method constraints (GET, POST, etc.). It should be easy to register new routes and provide a fallback for unmatched URLs.

## Requirements
- Implement a `Router` class with methods to register routes (e.g., `get()`, `post()`, `any()`).
- Support dynamic route parameters using a syntax like `/user/{id}` where `{id}` captures a segment of the URL.
- Extract and pass captured parameters to the associated callback function.
- Allow route callbacks to be either a callable (function/closure) or a string in the format `Controller@method`.
- Provide a method to dispatch the current request based on `$_SERVER['REQUEST_URI']` and `$_SERVER['REQUEST_METHOD']`.
- Return a 404 response (or invoke a user‑defined "not found" handler) when no route matches.
- Write clean, well‑documented code following PSR‑12 coding standards.

## Bonus
- Add support for optional route parameters (e.g., `/blog/{slug?}`).
- Implement route grouping with a common prefix and middleware (e.g., authentication check).
- Provide a simple way to generate URLs from route names (reverse routing).
- Include basic rate‑limiting middleware that can be attached to specific routes.