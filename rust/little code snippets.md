#### Return any error from a Result
```rust
use std::error::Error;
fn some_function() -> Result<(), box<dyn Error>> {}
```
#### Basic settings system
if you just want to modify things with a file, you can use `lazy_static!`, which creates only one struct/item which can be used to read the struct from all other threads.
```rust
use lazy_static::lazy_static;

lazy_static! {
pub static ref SETTINGS: AppSettings = AppSettings::new().expect("Config file is incorrect.");
}

```