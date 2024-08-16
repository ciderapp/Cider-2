# Cider-2

Cider-2 is a modern Apple Music app built using Vue.js, TypeScript, and an Electron/Tauri backend. It provides a sleek and intuitive user interface to enjoy your favorite music from the Apple Music library.

**Note: This readme file is for the public repository of Cider-2, which is used for issue tracking. The actual source code is not publicly available.**

## Relevant Repositories
- [Cider ThemeKit](https://github.com/ciderapp/cider-themekit)
  - Repository for tracking issues and feature requests for the theme system 
- [Cider PluginKit](https://github.com/ciderapp/Cider-PluginKit)
  - Repository for tracking issues and feature requests for the plugin system and API 

## Features

For a detailed list of features and functionalities, please visit the [Cider-2 website](https://www.cider.sh).

## Technologies Used

Cider-2 utilizes a range of technologies to deliver a seamless user experience:

- **Vue.js:** Vue.js is a popular JavaScript framework for building user interfaces. It offers a reactive and component-based architecture, making it ideal for creating dynamic web applications.

- **TypeScript:** TypeScript is a strongly-typed superset of JavaScript that enhances code quality and maintainability. It provides static type-checking, making it easier to catch errors during development.

- **Electron and Tauri:** Cider-2 leverages Electron for platforms other than Windows, while it uses Tauri specifically for the Windows platform. Electron is a framework for building cross-platform desktop applications using web technologies, and Tauri is a cross-platform framework that allows creating native Windows executables using web technologies.

## Installation

Cider-2 can be obtained through the following platforms:

- **Itch.io** Visit out page on [itch.io](https://cidercollective.itch.io/cider) where you can purchase Cider-2 for all platforms

- **Microsoft Store (Windows):** Visit the [Microsoft Store page](https://apps.microsoft.com/store/detail/cider-preview/9PL8WPH0QK9M?hl=en-us&gl=us&rtc=1) and follow the instructions to obtain and install Cider-2 for Windows.

- **Donation and Distribution (macOS, Windows, and Linux):** Cider-2 is available to donors through the official Discord server. Donors can access builds for macOS, Windows, and Linux. Join our official Discord server [here](https://discord.com/invite/AppleMusic) for more information.

*please note that we cannot transfer ownership between accounts, if you buy Cider on the Microsoft Store, we cannot transfer ownership to an itch.io account or vice versa*

## Main Missing Features Compared to standard Apple Music clients

1. **Lossless**: _Not currently possible in the MusicKit.js library due to there being no ability to decrypt the lossless music. We are working on implementing this with our own implementation of the MusicKit service. But this is still a while off._
2. **Crossfade**: _Same issue as above, we are limited on audio managing and modifying in MusicKit_
3. **Smart Playlists**: _This is a limitation of the API. Smart playlists are currently handled in Apple proprietary API which we do not have access to. We are working on our own in-house solution to this, but this is in early stages._
4. **Shared Playlists**: _Another API limitation, hopefully this will be rectified soon since this is a relatively new feature._

## FAQ

**1. Will Cider-2 support lossless audio?**

(See above)

**2. Why is Tauri not used on Linux?**

Tauri uses webkit2gtk, which does not support web security disabling, a requirement for Apple's API. Therefore, Tauri is not used on Linux for Cider-2.

**3. Is Cider-2 open-source?**

No, the source code of Cider-2 is not open-source. It is distributed under a proprietary license.

**4. Can donors distribute the builds of Cider-2?**

No, donors are not allowed to distribute the builds of Cider-2. The builds are provided exclusively to donors for personal use and are not intended for distribution.

**5. Will Crossfade be implemented?**

(See above)

**6. Is there going to be an EQ?**

An EQ is very possible in the future as we did have an implementation on Cider-1. However, the audio area of Cider-2 is in a reduced state, so this may be a while.

## License

Cider-2 is distributed under a proprietary license. The source code is not publicly available. Access to the builds is provided to donors and purchasers through the official Discord server, itch.io, and the Microsoft Store.

Please note that the distribution and use of Cider-2 builds obtained through these platforms are subject to the respective terms and conditions set by each platform. Make sure to review the license agreements and terms of service associated with the specific platform from which you obtained Cider-2.

## Acknowledgements

Cider-2 acknowledges the hard work and contributions of various open-source projects and libraries that have helped in its development.

## Contact

For any inquiries or support, please join our official Discord server [here](https://discord.com/invite/AppleMusic).
