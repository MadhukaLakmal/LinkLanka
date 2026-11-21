# LinkLanka Mobile Application

The cross-platform mobile client for LinkLanka, built with [React Native](https://reactnative.dev/) and [Expo](https://expo.dev/) (SDK 54).

## 📱 Features & Screens

- **Authentication**: Modern login and registration screens with JWT persistence in SecureStore.
- **Chat Interface**: High-performance chat view powered by `@shopify/flash-list` with support for text, voice notes, documents, and real-time Socket.io events.
- **Voice Messages**: Integrated audio recording (`expo-audio`), audio player context, and waveform visualization.
- **Magic Refine Modal**: Dialect and tone conversion modal for refining messages before sending.
- **Document Interrogation**: In-app document viewer and interactive AI question-answering modal.
- **Action Cards**: Direct 1-tap addition of detected meetings and reminders to the device calendar via `expo-calendar`.
- **Personal Slang Dictionary**: Management screen for custom user colloquialisms categorized into Singlish, Tanglish, and English buckets.
- **Theme Support**: Seamless Dark and Light theme switching via custom `ThemeContext`.

## 🛠️ Development

### Setup

```bash
# Install dependencies
bun install

# Start Expo development server
bun run start

# Launch on Android emulator/device
bun run android

# Launch on iOS simulator (macOS only)
bun run ios
```

### Environment Configuration

Copy the sample environment file:

```bash
cp .env.example .env
```

Ensure `EXPO_PUBLIC_API_URL` points to your backend instance:
- Android Emulator: `http://10.0.2.2:3000`
- Physical Device (same Wi-Fi): `http://<your-lan-ip>:3000`
- Production (Render): `https://your-api.onrender.com`
