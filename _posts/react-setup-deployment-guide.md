# React App Setup and Deployment Guide

This guide will walk you through setting up, running, and deploying your React application.

## Local Setup and Running

1. **Create React App**
   ```bash
   npx create-react-app your-app-name
   cd your-app-name
   ```

2. **Install Dependencies**
   ```bash
   npm install framer-motion lucide-react
   ```

3. **Set up Tailwind CSS**
   ```bash
   npm install -D tailwindcss postcss autoprefixer
   npx tailwindcss init -p
   ```

   Update `tailwind.config.js`:
   ```javascript
   module.exports = {
     content: ["./src/**/*.{js,jsx,ts,tsx}"],
     theme: { extend: {} },
     plugins: [],
   }
   ```

   Add to `src/index.css`:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

4. **Add Your React Component**
   Create `src/YourComponent.js` and add your component code.

5. **Update App.js**
   ```jsx
   import React from 'react';
   import YourComponent from './YourComponent';

   function App() {
     return (
       <div className="App">
         <YourComponent />
       </div>
     );
   }

   export default App;
   ```

6. **Run Locally**
   ```bash
   npm start
   ```

   View at: http://localhost:3000

## Deployment to GitHub Pages

1. **Create GitHub Repository**
   Create a new repository on GitHub.

2. **Initialize Git (if not already done)**
   ```bash
   git init
   ```

3. **Install GitHub Pages Package**
   ```bash
   npm install --save-dev gh-pages
   ```

4. **Update package.json**
   Add at the top level:
   ```json
   "homepage": "https://<username>.github.io/<repo-name>",
   ```
   Add to "scripts":
   ```json
   "predeploy": "npm run build",
   "deploy": "gh-pages -d build"
   ```

5. **Deploy**
   ```bash
   npm run deploy
   ```

6. **Configure GitHub Repository**
   - Go to repository settings
   - GitHub Pages section: set source to "gh-pages branch"

7. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```

Your app will be live at: https://<username>.github.io/<repo-name>

Remember to replace <username> and <repo-name> with your actual GitHub username and repository name.
