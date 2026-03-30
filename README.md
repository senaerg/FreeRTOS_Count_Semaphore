# FreeRTOS_Count_Semaphore
STM32 FreeRTOS Counting Semaphore Tasks Demo
# Quick Start
# STM32CubeIDE
1. Clone repo → Open .ioc file
2. Build → Flash to STM32 board
3. Open UART terminal (115200 baud)
4. Watch producer/consumer synchronization
# Features
✓ Proper semaphore initialization/cleanup
✓ Task priority inheritance awareness
✓ Infinite timeout handling (portMAX_DELAY)
✓ Stack overflow protection
✓ Deadlock prevention
✓ ISR-safe semaphore operations
✓ Configurable semaphore max count
# Build Target 
# Default (optimized)
make all

# Debug build
make DEBUG=1

# Different MCU
make MCU=STM32F103RB

# Expected Terminal Output
Producer Task1: Semaphore given (count=1)
Producer Task2: Semaphore given (count=2) 
Producer Task3: Semaphore given (count=3)
Consumer Task: Processing resource 1
Consumer Task: Processing resource 2
Consumer Task: Processing resource 3
Producer Task1: BLOCKED (max count reached)
[Tasks continue cycling...]
