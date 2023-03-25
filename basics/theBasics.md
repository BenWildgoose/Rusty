# The Basics

## Hello, World!

```
fn main() {
    println!("Hello, world!");
}
```

Defines the main function with `fn` and prints with `println!`.

`println!` is a **macro** because it ends in a `!`.


## Packages

The standard io is imported with `use std::io;`

### Random value generator 

- Import `use rand::Rng;`
- Then import the rand crate in Cargo.toml file, under dependencies `rand = "0.8.5"`

### Crates

Imported through Cargo.toml , can be found on [Crates.io](https://crates.io)


## Mutability

All variables in Rust are **immutable by default!**

An example of a mutable string is:

```
let mut name = String::new(); 
```

## Name input function

```
println!("What is your name?");
    let mut name = String::new();
    let greeting: &str = "Nice to meet you";
    io::stdin().read_line(&mut name)
        .expect("Didn't get an input!");

    println!("Hello {}! {}", name.trim_end(), greeting);
```

Firstly asks the users name. Then creates a mutable string (the input) and a immutable greeting symbol. Uses stdin from the stdio to read the line. Has a `.except` catch to tell users if they put no input in. Finally prints with {} to represent where the variables will go. `.trim_end()` gets rid of the new line character after the name.


## Constants

To make a constant unassigned integer of size 32 bits:
```
const ONE_MIL: u32 = 1000000;
```
> Floats of size 32 bits are denoted as `f32`

> To make a string just use `""`