#### Return any error from a Result
```rust
use std::error::Error;
fn some_function() -> Result<(), box<dyn Error>> {}
```
A `Box` stores things in the heap, the slower but dynamic and more-flexible area of memory. `Dyn` tells Rust that the size is dynamic, as any struct that applies the trait `Error` can be returned as a result.
#### Basic settings system
if you just want to read a configuration with a file, you can use `lazy_static!`, which creates only one struct/item which can be used to read the struct from all other threads. Combine this with the `config` module, and you have a super-simple configuration file. I prefer to use toml since that's what Rust uses, but it supports many file types and encodings.
```rust
use lazy_static::lazy_static;

struct AppSettings {
}

impl Default for AppSettings {
	fn default() -> Self {
		Self {}
	}
}
lazy_static! {
pub static ref SETTINGS: AppSettings = AppSettings::new().expect("Config file is incorrect.");
}

```
That crate in particular doesn't support writing to a file or anything. Which is why sometimes we may need to write our own logic for a settings system.