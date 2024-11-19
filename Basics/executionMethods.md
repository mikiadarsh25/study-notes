# Types of Code Execution

## 1. Compilation (Ahead-of-Time/AOT)

### Process

```
Source Code → Compiler → Machine Code → Execution
```

### Characteristics

-   **Speed**: Very fast execution
-   **Platform**: Machine-specific
-   **Memory**: Efficient memory usage
-   **Distribution**: Requires recompilation for different platforms

### Examples

```cpp
// C++ (Compiled Language) Example
#include <iostream>

int main() {
    int x = 10;
    std::cout << x << std::endl;
    return 0;
}
// Compiled to machine code before execution
```

### Advantages

-   Fastest runtime execution
-   Direct hardware interaction
-   Compile-time error detection
-   No runtime overhead

### Disadvantages

-   Platform dependent
-   Longer build time
-   Larger executable size
-   No runtime flexibility

## 2. Interpretation

### Process

```
Source Code → Interpreter → Execution
```

### Characteristics

-   **Speed**: Slower execution
-   **Platform**: Platform independent
-   **Memory**: Higher memory usage
-   **Distribution**: Source code or bytecode distribution

### Examples

```python
# Python (Interpreted Language) Example
x = 10
print(x)
# Executed line by line by interpreter
```

### Advantages

-   Platform independence
-   Immediate execution
-   Smaller program size
-   Dynamic typing support

### Disadvantages

-   Slower execution speed
-   Higher memory usage
-   Runtime overhead
-   No compile-time optimization

## 3. Just-In-Time (JIT) Compilation

### Process

```
Source Code → Bytecode → JIT Compiler → Machine Code → Execution
```

### Characteristics

-   **Speed**: Initially slower, then fast
-   **Platform**: Platform independent
-   **Memory**: Moderate to high usage
-   **Distribution**: Bytecode distribution

### Examples

```java
// Java (JIT Compiled) Example
public class Example {
    public static void main(String[] args) {
        int x = 10;
        System.out.println(x);
    }
}
// Compiled to bytecode, then JIT compiled during execution
```

### Advantages

-   Balance of performance and portability
-   Runtime optimization
-   Platform independence
-   Adaptive optimization

### Disadvantages

-   Initial overhead
-   Complex implementation
-   Memory overhead
-   Warmup time required

## 4. Hybrid Execution

### Process

```
Source Code → Multiple Execution Paths → Optimized Execution
```

### Characteristics

-   **Speed**: Variable based on path
-   **Platform**: Flexible
-   **Memory**: Variable usage
-   **Distribution**: Multiple formats possible

### Examples

```javascript
// JavaScript (Hybrid Execution) Example
function calculate(x) {
    return x * 2;
}

// Can be interpreted initially
// Then JIT compiled if frequently used
// May use AOT compilation for certain parts
```

## 5. Mixed-Mode Execution

### Process

-   Combines multiple execution methods
-   Switches between modes based on needs
-   Optimizes for different scenarios

### Examples

```java
// Java Mixed-Mode Example
class MixedMode {
    // Interpreted initially
    void rarely_called() {
        // Stays interpreted
    }

    // JIT compiled after threshold
    void frequently_called() {
        // Gets compiled to native code
    }
}
```

## Performance Comparison

### Execution Speed (Typical)

1. Compiled (AOT) - Fastest
2. JIT Compiled (After warmup) - Very Fast
3. Hybrid/Mixed-Mode - Fast
4. Interpreted - Slowest

### Memory Usage (Typical)

1. Compiled (AOT) - Lowest
2. Interpreted - Moderate
3. JIT Compiled - Higher
4. Hybrid/Mixed-Mode - Variable

## Use Cases

### Compiled Execution

-   System software
-   Performance-critical applications
-   Gaming engines
-   Operating systems

### Interpreted Execution

-   Scripting
-   Rapid prototyping
-   Educational purposes
-   Simple automation

### JIT Compilation

-   Enterprise applications
-   Web backends
-   Cross-platform applications
-   Cloud services

### Hybrid/Mixed-Mode

-   Modern web browsers
-   Complex applications
-   Mobile applications
-   Development environments
