Cargo has a config file, aka a manifest file, which helps to manage dependancies, compliation options, and package metadata, and is crucial when uploading your project to 'crates.io'.
\
**Cargo.toml:**
\
When making a project with cargo new, a default 'Cargo.toml' manifest file will be created witht he following structure:

```
[package]
name = "mybinary"
version = "0.1.0"
edition = "2021" 

[dependencies]# We can specify external dependencies here
```

If unfamiliar with the toml format, then use this resource to learn more about its syntax: https://toml.io/
\
**Metadata:**
\
The [package] table of our manifest file contains metadata about our crate.
\
Here is an overview of some of the most commonly encountered fields:

```
[package]
name = "mybinary"  # The crate name
version = "0.1.0"  # The crate's current version
edition = "2021"   # Which "Rust Edition" the crate utilizes 
description = ""   # A description of our crate for `crates.io`
keywords = ""      # Keywords for searches on `crates.io`
documentation = "" # URL to the crate's documentation
homepage = ""      # URL to the crate's homepage
repository = ""    # URL of the crate's source repositoryauthors = [""]     # The authors of the crate
license = ""       # The crate's license
rust-version = ""  # The minimum supported Rust version
```


**Rust Editions:**
\
The edition field denotes which Rust Edition the crate utilizes. Rust Editions are not the same as rustc compiler versions. Editions are released every few years and are indended mainly for backwards INCOMPATABLE changes to the language.
\
The 2021 edition will be in all the examples during the course. To view the specfic changes between Rust Editions you can use the command: "rustup doc --edition-guide".
\
**Dependencies:**
\
We can utilize external libraries by declaring them as dependencies. To declare a dependency, we add the crate name and the desired version number under the [dependencies] table.

```
[dependencies]
serde = "1.0.2"      # Uses version "1.0.2"
serde_derive = "1.0" # Uses version "1.0.X"
heck = "*"           # Uses version "X.X.X"
```

Versioning has a multitude of ways to deal with complex dependency resolution. More info about Cargo's demantic versioning can be found in "The cargo book" here:
https://doc.rust-lang.org/cargo/reference/resolver.html
\
When ading dependencies in this way, Cargo will automaticall yownload the source code for these libraries from crates.io and use them when compiling the crate.
\
You can also pull dependencies directly from a git repo with the git field:

```
serde = { git = "https://github.com/serde-rs/serde" } # A specific branch
serde = { git = "https://github.com/serde-rs/serde", branch = "next" } # A specific commit hash
serde = { git = "https://github.com/serde-rs/serde", rev = "7e19ae8c9486a3bbbe51f1befb05edee94c454f9" }
```

Pulling dependencies from the local file system is also possible with the 'path' field:

```
my_library = { path = "./../my_library" }
```

**Features:**
\
Some crates have parts of their library behind a feature gate. We can enable specific features with the 'features' field.

```
# The `features` field always takes an array of values
uuid = { version = "0.8", features = ["serde", "v4"] } # We can disable features that are added by default.
wee_alloc = { version = "0.4.5", default_features = false }
```

**Additional Configuration:**
You can do many other things with the manifest file such as specifying [dev-dependencies], declaring [features] for your own crate, creating a [profile] for specific compliation settings, and even making a [workspace] for manageing multiple crates within the same package.
\
For a comprehensive list of all available functionality, check out Cargo's guide for the Manifest Format here:
https://doc.rust-lang.org/cargo/reference/manifest.html
