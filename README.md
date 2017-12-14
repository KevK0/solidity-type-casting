# Solidity Type Casting
This repository allows to convert between the various types (string, address, uint ...) in solidity as hassle less as somehow possible. To achieve this I decided to create a simple to use library. This means that if library functions are called, their code is executed in the context of the calling contract, i.e. this points to the calling contract, and especially the storage from the calling contract can be accessed.

## Getting Started

These instructions will get your copy of the project up and running on your local machine for development purposes.

### Basic Usage

First import the corresponding casting library.

#### String Casting

```
import "github.com/KevK0/stringCasting.sol";

contract Contract {
    using stringcast for string;

    // ...
}
```

#### Address Casting

```
import "github.com/KevK0/addressCasting.sol";

contract Contract {
    using addresscast for string;

    // ...
}
```

The directive "using stringcast for string" can be used to attach library functions (from the library stringcast) to any type (string). These functions will receive the object they are called on as their first parameter (like the self variable in Python).

The effect of "using stringcast for string;" is that the functions from the library stringcast are attached to any type.

#### Example

In this basic Example we will convert the string str to uint.

```
string str = "123";
uint b = str.toUint();
```



