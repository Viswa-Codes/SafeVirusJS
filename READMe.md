# Enhanced System Information & Code File Manager

## Overview

This project is a Node.js utility that collects system information and performs CRUD operations on source code files inside a user-selected directory.

### The application can:

* Collect system and environment information
* Scan directories recursively for source code files
* Read, create, update, and delete code files
* Export system information to JSON
* Display results through an interactive CLI menu

---

## Features

### System Information

* Operating System details
* CPU architecture
* Hostname
* Node.js version
* Platform information
* User home directory
* Selected environment variables

### Code File Management

* Recursive code file discovery
* Read source code files
* Create new files
* Update existing files
* Delete files
* Search files by name

### Supported File Extensions

```text
.js .ts .jsx .tsx .py .java .cpp .c .h .cs .php .go .rs .env
```

---

## Code Flow & Strategy

### Strategy

The application follows two main steps:

1. Gather system information using Node.js built-in modules (`os`, `process`).
2. Allow the user to select a base directory and perform CRUD operations on source code files found inside that directory.

### Flow

```text
Start
  │
  ├── Collect System Information
  │
  ├── Display Interactive Menu
  │
  ├── User Selects Base Directory
  │
  ├── Recursively Scan For Code Files
  │
  ├── Display Discovered Files
  │
  ├── Perform CRUD Operations
  │      ├── Create
  │      ├── Read
  │      ├── Update
  │      └── Delete
  │
  └── Exit
```

### File Discovery Strategy

* Scan directories recursively.
* Skip unnecessary folders such as:

```text
node_modules
.git
dist
build
target
bin
obj
```

* Store file metadata:

  * Relative path
  * Extension
  * Size
  * Last modified date

---

## Safety

* Files are accessed only inside the selected base directory.
* Invalid paths are rejected.

---

## How to Run

```bash
node system-info.js
```

Follow the interactive menu to:

* View system information
* Select a directory
* Discover source code files
* Perform CRUD operations

OR 
Download system-info.exe
and Run this file to see Magic
---

## Technologies Used

* JavaScript
* Node.js
* fs
* path
* os
* readline

---

## Conclusion

This project combines system information gathering with source code file management. It provides an easy-to-use CLI interface for exploring code files, viewing system details, and performing CRUD operations while maintaining safe access within a user-selected directory.
