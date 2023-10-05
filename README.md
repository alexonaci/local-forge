# wa-forge

WIP

A WebAssebly ORM for writting SQLite queries. Can be used by web and mobile clients to query SQLite. It includes clients for Web (React and Angular), iOS, and Android, along with a Rust-based ORM package.

## Project Structure

Below is the directory layout for the project:

```plaintext
wa-forge/
├── pnpm-workspace.yaml
└── packages/
    ├── client/
    │   ├── typescript/
    │   │   └── frameworks/
    │   │       ├── react/
    │   │       │   └── package.json  (Thin client layer for React)
    │   │       └── angular/
    │   │           └── package.json  (Thin client layer for Angular)
    │   ├── android/
    │   │   └── build.gradle          (Wasm3, Android SQLite)
    │   └── iOS/
    │       └── Podfile               (SQLite.swift, Wasm3)
    ├── orm/
    │   └── Cargo.toml                (rusqlite, Diesel, wasm-bindgen, wasm-pack)
    └── shared/
        └── ...
```

## Setup

### Global Dependencies

1. Install PNPM:
    ```bash
    npm install -g pnpm
    ```

### WebAssembly (ORM)

Navigate to the `orm/` directory and build the Rust project with WebAssembly support:

```bash
wasm-pack build
```

### iOS Client

Navigate to the `client/iOS/` directory and install the required pods:

```bash
pod install
```

### Android Client

Open the `client/android/` directory in Android Studio and build the project.

### ORM

Navigate to the `orm/` directory and build the Rust project:

```bash
cargo build
```