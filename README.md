# Solidity Type Casting
This repository allows to convert between the various types (string, address, uint ...) in solidity as hassle less as somehow possible. To achieve this I decided to create a simple to use library. This means that if library functions are called, their code is executed in the context of the calling contract, i.e. this points to the calling contract, and especially the storage from the calling contract can be accessed.

## Getting Started

These instructions will get your copy of the project up and running on your local machine for development purposes.

### Basic Usage

First import the corresponding casting library.

#### String Casting

```
import "github.com/KevK0/contracts/stringCasting.sol";

contract Contract {
    using stringcast for string;

    // ...
}
```

#### Address Casting

```
import "github.com/KevK0/contracts/addressCasting.sol";

contract Contract {
    using addresscast for address;

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

## Usage

### String

#### To Address

```
string str = "0x0a723351e6637a1a519d0778acca42fa6af0b091";
address b = str.toAddress();
```

#### To Uint

```
string str = "123";
uint b = str.toUint();
```

#### Hex String To Bytes

```
string str = "0xa0cea4eac2896e97be887bab32c87a452aef12c69f587128fafd9143d94e5adc1eb7a2d48fc85f3ed8796599f73db394e2709ebfada127715b0bf21f00082e151c";
bytes b = str.toBytes();
```

#### To Lower Case

```
string str = "HELLO WoRlD";
str b = str.toLower();
// output -> hello world
```

#### To Upper Case

```
string str = "HELLO WoRlD";
str b = str.toUpper();
// output -> HELLO WORLD
```

### Address

#### To String

```
address addr = 0x3c36a0fb5c41685d5511d46bd53224910e4734d2;
string b = str.toString();
```

## Authors

* **Kevin Kaiser** - *Initial work* - [KevK0](https://github.com/KevK0)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
