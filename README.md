# input_simplified

A simple input handling crate for Rust.

## Usage

Add this to your `Cargo.toml`:

```toml
[dependencies]
input_simplified = "0.0.3"
```

```rust
use input_simplified::input;

fn main() {
    let name: String = input()
        .message("Enter your name: ")
        .get_input()
        .expect("Not a valid input");
    println!("Hello, {}!", name);

    let age: i32 = input()
        .message("Enter your age: ")
        .get_input()
        .expect("Not a valid input");
    println!("You are {} years old.", age);

    let height: f64 = input()
        .message("Enter your height in meters: ")
        .get_input()
        .expect("Not a valid input");
    println!("You are {} meters tall.", height);
}
```