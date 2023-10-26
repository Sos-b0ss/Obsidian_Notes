## Dependencies:

**These appear to be the dependencies for the Klondike game:**

[dependencies]
config = "~0.9"
derive_more = "~0.99"
directories = "~2.0"
euclid = "~0.20"
itertools = "~0.8"
lazy_static = "~1.4"
log = "~0.4"
log-panics = "~2.0"
num_enum = "~0.4"
num-traits = "~0.2"
rand = "~0.7"
simplelog = "~0.7"
serde = { version = "~1.0", features = ["derive"] }
snafu = "~0.6"
termion = "~1.5"

---

## Directory Tree:

**The file structure appears to look like:**
```
src[7]
	-display[10]
		-stack[4]
			-common.rs
			-horizontal.rs
			-mod.rs
			-vertical.rs
		-blank.rs
		-card.rs
		-frame.rs
		-game.rs
		-geometry.rs
		-help.rs
		-mod.rs
		-selector.rs
		-win.rs
	-model[8]
		-area[5]
			-foundation.rs
			-mod.rs
			-stock.rs
			-tableaux.rs
			-talon.rs
		-area_list.rs
		-card.rs
		-dealer.rs
		-game.rs
		-mod.rs
		-settings.rs
		-stack.rs
	-utils[5]
		-format_str.rs
		-mod.rs
		-str.rs
		-tuple.rs
		-vec.rs
	-engine.rs
	-lib.rs
	-main.rs
	-terminal.rs
```

## Agenda:

So for the most part I know that I should be able to get away with keeping things like `model/card.rs`, `model/dealer.rs`, `model/stack.rs`, `model/game.rs` the same because they are just cards and stacks of cards.
\
I'll need to look further into these to see what I should start trying to tweak a bit and see how I should implement things like "the player's hand" and 'the community cards'.
\
Then after making these tweaks I should go through and try to find how exactly It implements RNG for the deck, I have a feeling that would be located in the `src/engine.rs`
\
I also need to learn what engine the Rust app is running on and how that engine works for building TUI tools or games in the future.

## App Engine:

By the looks of it the app is tying the model and display by using:
- snafu
- std
- termion

Snip:
```
use snafu::ResultExt;
use std::{collections::HashMap, fmt, io};
use termion::event::Key;

use crate::{
    display::{
        game::{GameWidget, GameWidgetState},
        geometry, terminal_bounds, DisplayState,
    },
    model::{
        area::AreaId,
        dealer::{create_dealer, Dealer},
        game::{Action, Game},
        settings::GameSettings,
    },
    utils::tuple::both,
};

```

**Note the `::` in this snippet is the path separator for the 'crates'/'modules'/'ITEMS' structure it uses.

It also appears that the app is structuring its error handling using Debug, and Snafu:

Snip:
```

#[derive(Debug, Snafu)]
pub enum Error {
    #[snafu(display("IO error: {}", source))]
    IoError { source: io::Error },

    #[snafu(display("GameEngineBuilder: {}", message))]
    GameEngineBuilderError { message: String },
}

pub type Result<T, E = Error> = std::result::Result<T, E>;


```

