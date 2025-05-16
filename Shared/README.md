# Shared Modules

This directory includes utility code and shared libraries used across the backend and frontend applications.

## Examples

- `validators/` – Common request validation logic
- `auth/` – JWT creation and verification
- `constants/` – Role definitions, error messages
- `logger/` – Centralized logging functions

## Usage

All shared modules are written to be portable and versioned across services. Import only what is needed to reduce coupling.
