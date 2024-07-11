<h1 align="center">Code Segment</h1>

## Rust

##### 显示 FPS

```rust
let mut fps_timer = std::time::Instant::now();
let mut fps_counter = 0;

loop {
    fps_counter += 1;
    let elapsed = fps_timer.elapsed();

    if elapsed >= std::time::Duration::from_secs(1) {
        let fps = fps_counter as f64 / elapsed.as_secs_f64();
        window.set_title(&format!("Rust Game (FPS: {:.2})", fps));
        fps_counter = 0;
        fps_timer = std::time::Instant::now();
    }
}
```
