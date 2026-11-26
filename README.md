# KMP Delivery Management

A Kotlin Multiplatform (KMP) proof of concept for a delivery and order management system, developed as part of a collaborative software development project.

The project explores migrating an existing native Android application to a multiplatform architecture, enabling shared business logic, networking, and data management across Android and iOS.

## Features

- Authentication and session management.
- Order history and delivery logs.
- Search, filtering, sorting, and pagination.
- REST API integration using Ktor.
- Real-time updates through WebSocket communication.
- WebSocket reconnection handling.
- Location services and distance calculation.
- Network connectivity monitoring.
- Platform-specific secure storage.
- PDF generation and export on Android.

## Technologies

- Kotlin Multiplatform (KMP)
- Jetpack Compose
- Clean Architecture
- Ktor Client
- Koin Dependency Injection
- Kotlin Coroutines
- StateFlow
- Kotlinx Serialization
- WebSockets
- Google Maps
- Gradle Kotlin DSL

## Architecture

The project follows Clean Architecture principles, separating business logic, data management, and presentation responsibilities while maximizing code sharing across platforms.

| Layer | Responsibility |
|---|---|
| Presentation | UI state, ViewModels, and platform-specific interfaces |
| Domain | Business logic, use cases, models, and repository interfaces |
| Data | API integration, data sources, repositories, and serialization |
| Platform | Native implementations of location, storage, connectivity, and PDF services |

## Project Structure

```text
lmdkmp/
├── composeApp/
│   └── src/
│       └── androidMain/
├── shared/
│   └── src/
│       ├── commonMain/
│       ├── androidMain/
│       ├── iosMain/
│       └── commonTest/
└── iosApp/
```

## Multiplatform Approach

- **commonMain:** Shared business logic, domain models, repositories, networking, and state management.
- **androidMain:** Android-specific implementations and native service integrations.
- **iosMain:** Platform-specific implementations for iOS.
- **expect/actual:** Platform abstractions that enable shared code to access native functionality.

## Getting Started

The project requires Android Studio with Kotlin Multiplatform support, the appropriate platform SDKs, and backend service configuration.

Xcode is required for iOS development.

## Project Status

This project is a proof of concept exploring the migration from native Android development to Kotlin Multiplatform. Some iOS-specific implementations remain incomplete.

## Project Background

Developed collaboratively to explore multiplatform application architecture, shared business logic, and cross-platform development.

This fork preserves the original commit history and contributor attribution.
