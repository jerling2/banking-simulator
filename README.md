# Banking Simulator

A multithreaded banking simulation written in C. This project demonstrates the fundamentals of concurrent programming, thread synchronization, and resource sharing using POSIX threads (pthreads). Originally named "OS-MultiThreading," the project now focuses on simulating a simple banking environment where multiple clients perform transactions concurrently.

## Features

- Simulates multiple bank accounts.
- Supports concurrent deposit, withdrawal, and transfer operations.
- Demonstrates thread safety with mutexes and synchronization primitives.
- Detects and avoids common concurrency issues (e.g., race conditions, deadlocks).
- Extensible architecture for adding new transaction types or account features.

## Getting Started

### Prerequisites

- GCC or compatible C compiler
- POSIX Threads library (pthreads)
- Make (optional, for build automation)

### Building the Project

To build the simulator, clone the repository and run:

```bash
gcc -pthread -o banking_simulator main.c account.c transaction.c
```

Or, if a `Makefile` is provided:

```bash
make
```

### Running the Simulation

```bash
./banking_simulator
```

You may be able to configure the number of threads, accounts, or transactions via command-line arguments or configuration files (see code for details).

## Project Structure

```
.
├── main.c               # Entry point for the simulator
├── account.c/.h         # Bank account management
├── transaction.c/.h     # Transaction logic
├── thread_utils.c/.h    # Thread and synchronization helpers
├── README.md            # Project documentation
├── Makefile             # Build automation (if included)
```

## How It Works

- Each client is represented by a thread performing transactions on shared bank accounts.
- Mutexes ensure that account balances are updated safely.
- The simulation can be configured for different numbers of accounts, clients, and transaction types.

## Example Scenario

1. Multiple threads (clients) are started.
2. Each thread randomly deposits, withdraws, or transfers money between accounts.
3. All operations are logged and account balances are checked for consistency at the end.

## Customization

- Add new transaction types in `transaction.c`.
- Modify account properties or add logging in `account.c`.
- Tune thread and account counts in `main.c` or via command-line arguments.

## Contributing

Pull requests are welcome! Please open an issue first to discuss major changes.

## License

This project is licensed under the MIT License.
