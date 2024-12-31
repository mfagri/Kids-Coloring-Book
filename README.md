# Kids Coloring Book - Flutter App 🎨

A feature-rich Flutter coloring book application designed for children, featuring flood fill technology, custom color picker, and image management system.

![App Banner](https://raw.githubusercontent.com/mfagri/Kids-Coloring-Book/d279b3e104d97567937c4e36221573b30c8babc6/Group%203448.png)

## ✨ Features

- Interactive coloring experience with flood fill technology
- Kid-friendly UI with animations and visual feedback
- Custom color picker with predefined palettes
- Save and manage colored images
- Favorites system
- Undo/Redo functionality
- Image zooming and panning
- Progress saving
- Original/colored image toggle
- Share colored images
- Light/Dark mode support

## 📱 Screenshots

<table>
  <tr>
    <td><img src="https://github.com/mfagri/Kids-Coloring-Book/blob/main/Simulator%20Screenshot%20-%20iPhone%2015%20-%202024-12-16%20at%2018.59.54.png?raw=true" width="200"></td>
    <td><img src="https://github.com/mfagri/Kids-Coloring-Book/blob/main/Simulator%20Screenshot%20-%20iPhone%2015%20-%202024-12-16%20at%2019.00.14.png?raw=true" width="200"></td>
    <td><img src="https://github.com/mfagri/Kids-Coloring-Book/blob/main/Simulator%20Screenshot%20-%20iPhone%2015%20-%202024-12-16%20at%2019.00.21.png?raw=true" width="200"></td>
  </tr>
</table>

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (2.0.0 or higher)
- Dart SDK (2.12.0 or higher)
- Android Studio / VS Code
- iOS development tools (for iOS deployment)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/mfagri/Kids-Coloring-Book.git
```

2. Navigate to project directory:
```bash
cd kids_coloring_book
```

3. Install dependencies:
```bash
flutter pub get
```

4. Run the app:
```bash
flutter run
```

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.0
  shared_preferences: ^2.0.0
  path_provider: ^2.0.0
  flutter_colorpicker: ^1.0.0
  google_fonts: ^4.0.0
  permission_handler: ^10.0.0
  iconsax: ^0.0.8
```

## 🏗️ Project Structure

```
lib/
├── main.dart
├── screens/
│   ├── coloring/
│   │   ├── coloring_screen.dart
│   │   ├── coloring_gallery_screen.dart
│   │   └── widget/
│   ├── home/
│   │   └── home.dart
│   ├── edited_images_screen.dart
│   └── favorite_images_screen.dart
├── providers/
│   ├── edited_images_provider.dart
│   └── favorite_images_provider.dart
├── services/
│   ├── edited_images_service.dart
│   └── storage_service.dart
└── utils/
    └── image_flood_fill.dart
```

## 🛠️ Core Components

### Image Flood Fill

The core coloring mechanism uses a flood fill algorithm optimized for performance. Three implementations are provided:
- Basic recursive flood fill
- Queue-based flood fill
- Span-based flood fill (recommended)

```dart
class ImageFloodFillSpanImpl extends FloodFill<ui.Image, Color> {
  ImageFloodFillSpanImpl(super.image);

  @override
  Future<ui.Image?> fill(int startX, int startY, Color newColor) async {
    // Implementation details in utils/image_flood_fill.dart
  }
}
```

### Color Picker

Custom color picker features:
- Pre-defined color palettes
- Custom color creation
- Color wheel and grid views
- Recent colors history

## 📱 State Management

The app uses Provider for state management with two main providers:
- `EditedImagesProvider`: Manages saved colored images
- `FavoriteImagesProvider`: Handles favorite images

## 💾 Local Storage

The app uses SharedPreferences for persistent storage:
- Edited images paths
- Favorite images paths
- User preferences

## ⚙️ Customization

### Theming

Customize the app's appearance by modifying the theme in `main.dart`:

```dart
ThemeData(
  colorScheme: ColorScheme.fromSeed(
    seedColor: Colors.white,
    primary: Colors.amber,
    // Customize colors here
  ),
  // More theme customization
)
```

### Adding New Images

To add new coloring pages:
1. Add images to `assets/coloring_pages/`
2. Update the `pubspec.yaml` file
3. Add image paths to the gallery list in `ColoringGalleryScreen`

### Modifying Color Palettes

Customize the color palettes in `ColorPicker`:

```dart
static final List<List<Color>> _colorPalettes = [
  // Modify color palettes here
];
```

## 🧪 Running Tests

```bash
flutter test
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact & Support

For support, questions, or bug reports:

- 📧 Email: marouane.fagri1@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/mfagri/Kids-Coloring-Book/issues)

## ⭐ Show your support

Give a ⭐️ if this project helped you!

## 📝 Changelog

- **v1.2.0**
  - Implemented favorites system
  - Bug fixes and performance improvements

- **v1.1.0**
  - Added undo/redo functionality
  - Enhanced color picker interface

- **v1.0.0**
  - Initial release
  - Basic coloring functionality
  - Image saving and sharing

---
Created with ❤️ by [mfagri]
