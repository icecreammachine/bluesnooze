![Bluesnooze logo](images/icon.png)

# Bluesnooze

Please note the latest release requires MacOS Sequoia (15.0) or higher.

## About

**Bluesnooze prevents your sleeping Mac from connecting to Bluetooth accessories.**

If you pair Bluetooth headphones or speakers with both your phone & Mac it can be frustrating when your sleeping Mac connects intermittently and disrupts the audio.

With Bluesnooze the Bluetooth connection is switched off when your Mac sleeps, and switched on when your Mac wakes.

![Screenshot showing Bluesnooze in the status bar](images/screenshot.png)

## Installation

1. Download `Bluesnooze.zip` from the [latest release][download-latest]
1. In Finder, open `Bluesnooze.zip` in your `Downloads` directory
1. Drag `Bluesnooze.app` to your `Applications` directory

## Caveats

- Unfortunately this app can't be distributed via the App Store because it uses a private API to switch Bluetooth on/off (but the release version is notarized by Apple).

[download-latest]: https://github.com/icecreammachine/bluesnooze/releases

## FAQs

### How can I hide the Bluesnooze icon?

In your terminal run the following command:

```sh
defaults write com.oliverpeate.Bluesnooze hideIcon -bool true && killall Bluesnooze
```

When you next relaunch the application there should be no icon in the menu bar.

### How can I restore the Bluesnooze icon?

In your terminal run the following command:

```sh
defaults delete com.oliverpeate.Bluesnooze hideIcon && killall Bluesnooze
```

When you next relaunch the application it should appear in the menu bar.
