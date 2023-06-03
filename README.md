# Cider-2

Cider-2 is a modern Apple Music app built using Vue.js, TypeScript, and an Electron/Tauri backend. It provides a sleek and intuitive user interface to enjoy your favorite music from the Apple Music library.

**Note: This readme file is for the public repository of Cider-2, which is used for issue tracking, discussions, and feature requests. The actual source code is not publicly available.**

## Features

For a detailed list of features and functionalities, please visit the [Cider-2 website](https://www.cider.sh).

## Technologies Used

Cider-2 utilizes a range of technologies to deliver a seamless user experience:

- **Vue.js:** Vue.js is a popular JavaScript framework for building user interfaces. It offers a reactive and component-based architecture, making it ideal for creating dynamic web applications.

- **TypeScript:** TypeScript is a strongly-typed superset of JavaScript that enhances code quality and maintainability. It provides static type-checking, making it easier to catch errors during development.

- **Electron and Tauri:** Cider-2 leverages Electron for platforms other than Windows, while it uses Tauri specifically for the Windows platform. Electron is a framework for building cross-platform desktop applications using web technologies, and Tauri is a cross-platform framework that allows creating native Windows executables using web technologies.

## Installation

Cider-2 can be obtained through the following platforms:

- **Steam:** Visit the [Steam store page](https://store.steampowered.com/app/2446120/Cider) and follow the instructions to purchase and install Cider-2.

- **Microsoft Store (Windows):** Visit the [Microsoft Store page](https://apps.microsoft.com/store/detail/cider-preview/9PL8WPH0QK9M?hl=en-us&gl=us&rtc=1) and follow the instructions to obtain and install Cider-2 for Windows.

- **Donation and Distribution (macOS and Linux):** Cider-2 is available through donation and distribution in the official Discord server. To obtain Cider-2 for macOS and Linux, make a donation through GitHub, OpenCollective, or Ko-Fi, and join our official Discord server [here](https://discord.com/invite/AppleMusic) for verification and access to the builds.

## FAQs

**1. Will Cider-2 support lossless audio?**

Currently, lossless playback is not supported in Cider-2. While Apple's MusicKit Framework does have lossless support, decryption of this audio is not currently supported.

**2. Why is Tauri not used on Linux?**

Tauri uses webkit2gtk, which does not support web security disabling, a requirement for Apple's API. Therefore, Tauri is not used on Linux for Cider-2.

**3. Is Cider-2 open-source?**

No, the source code of Cider-2 is not open-source. It is distributed under the Affero General Public License (AGPL-3.0), which allows individuals who obtain the software to use, modify, and distribute it under certain conditions.

## License

Cider-2 is distributed under the [AGPL-3.0 License](https://www.gnu.org/licenses/agpl-3.0.en.html).

## Acknowledgements

Cider-2 acknowledges the hard work and contributions of various open-source projects and libraries that have helped in its development.

## Contact

For any inquiries or support, please join our official Discord server [here](https://discord.com/invite/AppleMusic).
