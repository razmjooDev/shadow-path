# Shadow Path

A privacy-focused VPN application for Android, forked from ProtonVPN.

## About

Shadow Path is built upon the open-source ProtonVPN Android application, providing secure and private internet access.

## Screenshots

<p align="center">
    <img src="https://raw.githubusercontent.com/ProtonVPN/android-app/master/metadata/en-US/images/phoneScreenshots/2.jpg" height="400">
    <img src="https://raw.githubusercontent.com/ProtonVPN/android-app/master/metadata/en-US/images/phoneScreenshots/3.jpg" height="400">
    <img src="https://raw.githubusercontent.com/ProtonVPN/android-app/master/metadata/en-US/images/phoneScreenshots/4.jpg" height="400">
    <img src="https://raw.githubusercontent.com/ProtonVPN/android-app/master/metadata/en-US/images/phoneScreenshots/5.jpg" height="400">
</p>

## Build Instructions

### Prerequisites
- Android SDK
- Android NDK
- CMake
- SWIG

### Debug Build
1. Clone this repository
2. Run: `./gradlew assembleProductionVanillaOpenSourceDebug`

   Or open the project in Android Studio and build from there

### Release Build
To build a release version, you need to provide signing keys:

```bash
./gradlew assembleProductionVanillaOpenSourceRelease \
  -PkeyStoreFilePath=<keystore> \
  -PkeyStoreKeyAlias=<alias> \
  -PkeyStorePassword=<pass> \
  -PkeyStoreKeyPassword=<key-pass>
```

## Code Style

### Java
Import the ProtonStyle.xml code style in Android Studio:
```
File >> Settings >> Editor >> Code Style >> Import Scheme
```

### Kotlin
The project uses ktlint with default rules for Kotlin code formatting.

## Contributing

We welcome contributions! Please follow these guidelines:

- Adhere to the project's existing code style and naming conventions
- New code should be written in Kotlin where possible (we're transitioning from Java)
- Use our preferred tech stack: Kotlin, MVVM, data-binding, and coroutines
- After updating open source dependencies, run `gradlew updateLicensesJson` to update attributions

### Running Tests Locally

```bash
gradlew checkstyle
gradlew detekt
gradlew test
gradlew androidTest
```

### Contribution Agreement

By contributing to this project, you agree to the following:

1. I assign any and all copyright related to the contribution to the project maintainers
2. I certify that the contribution was created in whole by me
3. I understand and agree that this project and the contribution are public and that a record of the contribution (including all personal information I submit with it) is maintained indefinitely and may be redistributed with this project or the open source license(s) involved

## Versioning

Version format: `[major][minor][patch][hotfix]`

## License

The code and datafiles in this distribution are licensed under the terms of the GPLv3 as published by the Free Software Foundation. See <https://www.gnu.org/licenses/> for a copy of this license.

Original code copyright (c) 2019 Proton AG

---

**Note:** This is a fork of the ProtonVPN Android application. The original project can be found at [ProtonVPN/android-app](https://github.com/ProtonVPN/android-app).