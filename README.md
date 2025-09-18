# Simple Notes App

A modern, responsive notes application built with Next.js, featuring dark mode, search functionality, and local storage persistence.

## 🚀 Features

- **Create & Manage Notes**: Add new notes with title and content
- **Edit & Delete**: Inline editing and deletion of existing notes
- **Search & Filter**: Real-time search across note titles and content
- **Dark Mode**: Toggle between light and dark themes with system preference detection
- **Responsive Design**: Optimized for mobile, tablet, and desktop devices
- **Form Validation**: Required title validation with error handling
- **Local Persistence**: Notes are saved to browser's local storage

## 🛠️ Tech Stack

- **Framework**: Next.js 13+ with App Router
- **Styling**: Tailwind CSS with shadcn/ui components
- **Icons**: Lucide React
- **Storage**: Local Storage (easily replaceable with MongoDB)
- **TypeScript**: Full type safety

## 🏃‍♂️ Quick Start

### Prerequisites

- Node.js 18+ installed on your machine
- npm or yarn package manager

### Installation

1. Clone this repository:
```bash
git clone <your-repo-url>
cd simple-notes-app
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Start the development server:
```bash
npm run dev
# or
yarn dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🗃️ MongoDB Integration

Currently, the app uses local storage for persistence. To integrate with MongoDB:

### Option 1: MongoDB Atlas (Recommended)

1. Create a MongoDB Atlas account at [mongodb.com/atlas](https://mongodb.com/atlas)
2. Create a new cluster and get your connection string
3. Install MongoDB dependencies:
```bash
npm install mongodb mongoose
```

4. Create a `.env.local` file:
```env
MONGODB_URI=your_connection_string_here
```

5. Replace the local storage logic with MongoDB operations using the API routes pattern.

### Option 2: Local MongoDB

1. Install MongoDB locally
2. Update connection string to point to your local instance
3. Follow the same integration steps as above

## 📱 Usage

### Creating Notes
- Click the "New Note" button
- Enter a title (required) and content
- Click "Create Note" to save

### Editing Notes
- Hover over any note card and click the edit icon
- Make your changes inline
- Click "Save" to confirm or "Cancel" to discard changes

### Searching Notes
- Use the search bar to filter notes by title or content
- Search is real-time and case-insensitive

### Dark Mode
- Toggle dark mode using the moon/sun icon in the header
- Respects your system's dark mode preference by default

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to a GitHub repository
2. Connect your GitHub account to Vercel
3. Import your repository
4. Configure environment variables if using MongoDB
5. Deploy!

### Other Platforms

The app can be deployed to any platform that supports Next.js static exports:
- Netlify
- GitHub Pages
- AWS S3 + CloudFront
- Firebase Hosting

## 🏗️ Architecture Decisions

### 1. Local Storage vs Database
- **Current**: Local storage for simplicity and immediate functionality
- **Future**: Easy migration to MongoDB with minimal code changes
- **Benefits**: No setup required, works offline, fast performance

### 2. Component Architecture
- **Single Page Application**: All functionality in one component for simplicity
- **Modular UI**: Uses shadcn/ui components for consistency
- **Type Safety**: Full TypeScript integration

### 3. State Management
- **React useState**: Sufficient for current app complexity
- **Local Storage Sync**: Automatic persistence without external dependencies
- **Future**: Easy to migrate to Redux/Zustand if needed

### 4. Styling Approach
- **Tailwind CSS**: Utility-first approach for rapid development
- **CSS Variables**: Dark mode implementation with smooth transitions
- **Responsive Design**: Mobile-first approach with breakpoints

### 5. Validation Strategy
- **Client-side Only**: Real-time validation for better UX
- **Required Fields**: Title validation prevents empty notes
- **Future**: Server-side validation when adding backend

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔮 Future Enhancements

- [ ] MongoDB integration with API routes
- [ ] User authentication
- [ ] Note categories/tags
- [ ] Export notes (PDF, Markdown)
- [ ] Rich text editor
- [ ] Note sharing functionality
- [ ] Offline sync
- [ ] Mobile app (React Native)

---

Built with ❤️ using Next.js and Tailwind CSS