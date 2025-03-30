![Screenshot_2025-03-30-23-23-03-26_4f5da45ba9f8f23938554d03350e5c8d~3](https://github.com/user-attachments/assets/36a2c95d-1f6f-4096-91b3-be7f4bb01221)# News Room Application

## Overview
News Room is a mobile application developed using Flutter that provides users with the latest news from various sources. This project was developed as part of the Mandiri Virtual Internship Program, implementing clean architecture principles and modern design patterns.

## Features
- Latest news feed with infinite scrolling
- News categorization (Business, Technology, Sports, etc.)
- Article bookmarking functionality
- Detailed article view
- Search news articles
- Clean and intuitive user interface

## Architecture
The application follows Clean Architecture principles with MVVM (Model-View-ViewModel) pattern:
```
lib/![Uploading Screenshot_2025-03-30-23-23-03-26_4f5da45ba9f8f23938554d03350e5c![Uploading Screenshot_2025-03-30-23-23-12-59_4f5da45ba9f8f23938554d03350e5c8d~2.jpg…]()
8d~3.jpg…]()

├── data/
│   ├── models/
│   ├── repositories/
│   └── sources/
├── domain/
│   ├── entities/
│   ├── repositories/
│   └── usecases/
├── presentation/
│   ├── pages/
│   ├── widgets/
│   └── viewmodels/
└── core/
    ├── utils/
    ├── constants/
    └── themes/
```

## Tech Stack
- Flutter
- Dart
- Provider (State Management)
- Dio (Network Calls)
- SQLite (Local Storage)
- GetIt (Dependency Injection)

## Getting Started

### Prerequisites
- Flutter SDK
- Android Studio / VS Code
- Git

### Installation
1. Clone the repository
```bash
git clone https://github.com/yourusername/news-room-app.git
```

2. Navigate to project directory
```bash
cd news-room-app
```

3. Install dependencies
```bash
flutter pub get
```

4. Run the app
```bash
flutter run
```

## Design Patterns Used
- Repository Pattern
- Factory Pattern
- Singleton Pattern
- Observer Pattern
- Dependency Injection

## Features Screenshots
| Home Screen | Article Detail |
|-------------|----------------|
| [Home Image] | [Detail Image]

## Code Standards
- Followed Dart's official style guide
- Implemented proper error handling
- Used meaningful variable and function names
- Added comments for complex logic
- Proper file and folder structure

## Testing
The application includes:
- Unit Tests
- Widget Tests
- Integration Tests

## Performance Optimization
- Lazy loading of images
- Caching mechanisms
- Efficient state management
- Optimized build methods

## Contributing
1. Fork the Project
2. Create your Feature Branch
3. Commit your Changes
4. Push to the Branch
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments
- News API for providing the news data
- Bank Mandiri for the internship opportunity
- Flutter community for resources and support

## Contact
Reyhan Capri Moraga - [@reannn22](https://github.com/Reannn22)

Project Link: [https://github.com/Reannn22/Bank-Mandiri-Internship-Task-Final-Task-UI-and-Design-Pattern](https://github.com/yourusername/news-room-app)
