# homebrew-lazymacfan

Homebrew tap for [lazymacfan](https://github.com/zeetec20/lazymacfan) — a lightweight macOS TUI and background fan
controller.

## Install

```bash
brew tap zeetec20/lazymacfan
brew install lazymacfan
```

Or in one command:

```bash
brew install zeetec20/lazymacfan/lazymacfan
```

## Background service

```bash
brew services start lazymacfan
brew services stop lazymacfan
```

Don't also run `lazymacfan service start`: that installs a second launchd job
(`com.lazymacfan.agent`) and the two will fight over fan control.

## Privileged helper

Writing fan speeds needs root. Authorize the helper once:

```bash
lazymacfan helper setup
```

## Upgrade

```bash
brew update && brew upgrade lazymacfan
```

## Uninstall

```bash
lazymacfan uninstall          # removes the launchd job and the privileged helper
brew uninstall lazymacfan
```

`Formula/lazymacfan.rb` is generated and pushed by the release workflow in
[zeetec20/lazymacfan](https://github.com/zeetec20/lazymacfan) — don't edit it by hand.
