# Banking Simulator

A multithreaded banking simulation written in C. This project demonstrates the fundamentals of concurrent programming, thread synchronization, and resource sharing using POSIX threads (pthreads). The focus is on simulating a simple banking environment where multiple clients perform transactions concurrently.

## Features

- Simulates multiple bank accounts.
- Supports concurrent deposit, withdrawal, and transfer operations.
- Demonstrates thread safety with mutexes and synchronization primitives.
- Detects and avoids common concurrency issues (e.g., race conditions, deadlocks).
- Extensible architecture for adding new transaction types or account features.
- Heavy use of multi-threading to model real-world concurrent banking operations.

## Getting Started

### Prerequisites

- GCC or compatible C compiler
- POSIX Threads library (pthreads)

## Project Structure

```
.
├── part1/                # Single-threaded and basic multi-threaded implementation
├── part2/                # Multi-threaded implementation
├── part3/                # Multi-threaded with more advanced synchronization
├── part4/                # Multi-threaded with inter-process communication
├── README.md             # Project documentation
```

## How It Works

- Each client or worker is represented by a thread performing transactions on shared bank accounts.
- Mutexes ensure that account balances are updated safely.
- The simulation can be configured for different numbers of accounts, clients, and transaction types.

## Example Scenario

1. Multiple threads (clients) are started.
2. Each thread deposits, withdraws, or transfers money between accounts.
3. All operations are logged and account balances are checked for consistency at the end.

## License

This project is licensed under the MIT License.
