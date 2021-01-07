# Klarna Mobile SDK Build Variants

Until the release of Swift 5.1, all Swift modules in a project had to be built with (roughly) the
same version of Swift.

While this is not an issue from 5.1 onwards, we offer support for older versions. We also do this
to (if needed) release versions built against beta versions of Xcode. Support for this is available
through Cocoapods, Carthage as well as manual (drag-and-drop) integrations.

We do this by providing multiple builds made with several versions of Xcode as well as fat (device +
simulator) and slim (device-only) builds.

## Variants

For this release, we provide:

| Name | Fat/slim | Xcode Ver. & Build No. | Swift Ver. | Swift Toolchain Ver. |
| ---- | -------- | ---------------------------- | ---------- | -------------------- |
| `xcode-11.3.1-fat` | fat | 11.3.1 - 11C505 | 5.1.3| swiftlang-1100.0.282.1 clang-1100.0.33.15 |
| `xcode-11.3.1-slim` | slim | 11.3.1 - 11C505 | 5.1.3| swiftlang-1100.0.282.1 clang-1100.0.33.15 |
| `xcode-11.7-fat` | fat | 11.7 - 11E801a | 5.2.4| swiftlang-1103.0.32.9 clang-1103.0.32.53 |
| `xcode-11.7-slim` | slim | 11.7 - 11E801a | 5.2.4| swiftlang-1103.0.32.9 clang-1103.0.32.53 |
| `xcode-12.2-fat` | fat | 12.2 - 12B45b | 5.3.1| swiftlang-1200.0.41 clang-1200.0.32.8 |
| `xcode-12.2-slim` | slim | 12.2 - 12B45b | 5.3.1| swiftlang-1200.0.41 clang-1200.0.32.8 |


## Cocoapods

This release defaults to using the latest, non-beta version `xcode-12.2-fat`. If you
want to use a different variant, update your Podfile to use a different subspec. E.g:


```ruby
pod 'KlarnaMobileSDK/xcode-11.3.1-fat', '~> 2.0.30'
```

```ruby
pod 'KlarnaMobileSDK/xcode-11.7-fat', '~> 2.0.30'
```

```ruby
pod 'KlarnaMobileSDK/xcode-12.2-fat', '~> 2.0.30'
```

