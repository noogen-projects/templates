# Noogen crate templates

Use [`cargo-generate`](https://github.com/ashleygwilliams/cargo-generate) to generate a new Rust project by template from one of git repository:

```
cargo generate --git https://github.com/noogen-projects/lib-template.git -n projectname
```

To simplify generation command line, add the `noogen` cargo command as below:

```
cat > ~/.cargo/bin/cargo-noogen << EOM
#!/bin/sh
cargo generate --git https://github.com/noogen-projects/\${2}-template.git -n \${3}
EOM
chmod a+x ~/.cargo/bin/cargo-noogen
```

Usage:

```
cargo noogen lib projectname
```
