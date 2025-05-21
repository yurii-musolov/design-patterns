# Adapter

The Adapter acts as a wrapper between two objects. It catches calls for one object and transforms them to format and interface recognizable by the second object.

In this example, the trait SpecificTarget is incompatible with a call function which accepts trait Target only.

```rs
fn call(target: impl Target);
```

The adapter helps to pass the incompatible interface to the call function.

```rs
let target = TargetAdapter::new(specific_target);
call(target);
```

Run

```bash
cargo run --bin adapter
```

Output

```bash
A compatible target can be directly called: 'Ordinary request.'
Adaptee is incompatible with client: '.tseuqer cificepS'
But with adapter client can call its method: 'Specific request.'
```
