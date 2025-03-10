# Nudger App

##Log
Day 1 : Vibe coded with cursor AI and was almost ready. Then I ran into weird space and configuration issue between android stuio and cursor

##Inspiration
With all the talk around Vibe Coding, I wanted to check I can also build something for my own. This is going to be my first android project and I will use cursor to build it without coding. The core feature of this project "Nudge" was a feature that existed in now extinct app "Hike". All you need to do is double tap on a chat with a person and they will get a vibrating notification.Sort of a virtual tap on the shoulder. This is something that my partner used to like a lot. Lets see if I cab bring it back into existence

## Overview
Nudger is a lightweight Android application built using Flutter that allows users to select a contact and send them a 'nudge'. A nudge triggers a vibration and screen shake effect on the recipient's device if they also have the app installed. This project started with a larger vision of including server components but is currently focused on peer-to-peer (P2P) communication using Wi-Fi Direct.

## Project Evolution
Initially, the plan was to implement the Nudge feature using a centralized backend for storing contacts, managing notifications, and ensuring smooth communication. However, in order to make the app faster, privacy-focused, and server-independent, the development strategy was revised to use Wi-Fi Direct for direct device-to-device communication.

### **Phase 1: Wi-Fi Direct Communication (Current Phase)**
- Use Wi-Fi Direct (P2P) to send nudges without requiring internet connectivity.
- Enable device discovery and selection without explicit pairing.
- Send targeted nudges only to selected contacts.
- Ensure seamless real-time nudging with minimal latency.

### **Future Phases (Possible Expansions)**
- **Phase 2:** Implement Bluetooth Low Energy (BLE) as an alternative for short-range nudging.
- **Phase 3:** Introduce optional backend support for remote nudging over the internet.
- **Phase 4:** Expand functionality to include multimedia nudging (custom vibration patterns, sound alerts, etc.).

## Tech Stack
- **Framework:** Flutter (Dart)
- **Networking:** Wi-Fi Direct (`flutter_wifi_p2p` package)
- **State Management:** Riverpod or Provider
- **Permissions Required:** Contacts access, Wi-Fi Direct, Location (for device discovery)

## Features
- **Select a Contact** – Users can browse and select a contact from their list.
- **Send a Nudge** – Initiates a Wi-Fi Direct message to the selected contact’s device.
- **Receive a Nudge** – When a nudge is received, the device vibrates and performs a subtle shake animation.
- **No Pairing Required** – Unlike Bluetooth, no explicit pairing is needed; devices are discovered and nudges are sent directly.

## Security & Privacy Considerations
- No backend storage – all user data remains on the device.
- Contacts are matched locally and never uploaded to a server.
- Basic encryption is planned for future phases to secure Wi-Fi Direct communication.

## Installation
### Prerequisites
- Android device running Android 8.0+ (Wi-Fi Direct support required)
- Flutter SDK installed ([Installation Guide](https://flutter.dev/docs/get-started/install))

### Running the App
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/nudge-app.git
   ```
2. Navigate to the project directory:
   ```sh
   cd nudge-app
   ```
3. Install dependencies:
   ```sh
   flutter pub get
   ```
4. Run the app:
   ```sh
   flutter run
   ```

## Development Strategy
- **Step 1:** Implement UI (Contact selection and nudge button)
- **Step 2:** Implement Wi-Fi Direct targeted messaging for communication
- **Step 3:** Optimize message delivery and background reception
- **Step 4:** Test thoroughly and deploy

## Contributing
Contributions are welcome! Feel free to submit issues, feature requests, or pull requests to improve the project.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References
- [Flutter Wi-Fi P2P](https://pub.dev/packages/flutter_wifi_p2p)
- [Flutter Contacts Plugin](https://pub.dev/packages/contacts_service)
- [Vibration Plugin](https://pub.dev/packages/vibration)

