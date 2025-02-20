# rsvm

A version manager for rust.

## Installation

```console
curl -L https://raw.github.com/paulgg-code/rsvm/master/install.sh | sh
```

or

```console
wget -qO- https://raw.github.com/paulgg-code/rsvm/master/install.sh | sh
```

### for fish-shell users

```console
ln -s ~/.rsvm/rsvm.fish ~/.config/fish/functions
```

or

```console
echo "source ~/.rsvm/rsvm.fish" >> ~/.config/fish/config.fish
```

## Usage

Show the help messages. Choose the one that you like most.

```console
rsvm help
rsvm --help
rsvm -h
```

Download and install a &lt;version&gt;. &lt;version&gt; could be for example "0.12.0".

```console
rsvm install <version>
e.g.: rsvm install 1.70.0
```

Activate &lt;version&gt; for now and the future.

```console
rsvm use <version>
e.g. rsvm use 1.70.0
```

List all installed versions of rust. Choose the one that you like most.

```console
rsvm ls
rsvm list
```

List all versions of rust that are available for installation.

```console
rsvm ls-remote
```

Print a channel version of rust that is available for installation.

```console
rsvm ls-channel stable
```

## Example: Install 1.70.0

```console
curl https://raw.github.com/paulgg-code/rsvm/master/install.sh | sh
source ~/.rsvm/rsvm.sh
rsvm install 1.70.0
rsvm use 1.70.0

# you will now be able to access the rust binaries:
~ ∴ rustc -v
rustc 1.70.0
host: x86_64-apple-darwin

~ ∴ cargo -h
Usage: cargo <cmd> [options] [args..]

~ ∴ rustdoc -h
Usage: rustdoc [options] <cratefile>
```

## Running the tests

RSVM is tested with bats. Install like this:

```console
git clone https://github.com/sstephenson/bats.git
cd bats
./install.sh /usr/local
```

Inside the rsvm repository do this:

```console
bats test/rsvm.sh.bats
```

## License

Hereby placed under MIT license.
