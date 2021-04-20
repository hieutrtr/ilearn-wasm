### Generate from template
```
cargo install cargo-generate

cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

### Dependencies
* wasm-bindgen : allow us to use `#[wasm-bindgen]` represent interface we want between Javascript and Rust (wasm). Simply to say that the function below that tag can be accessible from both Javascript and Rust.
```
#[wasm_bindgen]
extern {
    fn alert(s: &str); // JS function
}
```

* Above code is to import alert function from JS.

```
#[wasm_bindgen]
pub fn greet() {
    alert("Hello, test-wasm!");
}
```

* Above code mean rust can call alert function and witt wasm_bindgen tag JS can also call greet function.