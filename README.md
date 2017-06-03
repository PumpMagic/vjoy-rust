# Directory Tree
* src: Rust sources
* vjoy-headers: vJoy C header files
    * original: original vJoy headers
    * bindgen: vJoy headers modified to work with bindgen

# Building
To make ```src/vjoy_bindgen.rs``` (do this if and only if that file doesn't already exist):

1. ```cd <repository root>```
1. ```bindgen vjoy-headers/bindgen/vjoy.h -o src/vjoy_bindgen.rs```
1. Add lint attributes to ```src/vjoy_bindgen.rs```:
    ```rust
    #![allow(dead_code)]
    #![allow(non_snake_case)]
    #![allow(non_camel_case_types)]
    ```

To build crate:
1. ```cd <repository root>```
1. ```cargo build```