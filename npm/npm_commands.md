# NPM Command Reference

## Setup & Installation

### Install Dependencies from package.json
Installs all dependencies listed in your existing `package.json` file.
`npm install`

### Initialize Project
Create `package.json` with defaults.
`npm init -y`

### Install New Dependency
Adds a package to `dependencies` in `package.json`.
`npm install <package_name>`

### Install Dev Dependency
Adds a package to `devDependencies` (for testing, linting, etc.).
`npm install -D <package_name>`

### Install Specific Version
`npm install <package_name>@<version>`

## Common Scripts

### Run Development Server
Starts the local development server (common in Vite, Next.js, React).
`npm run dev`

### Build for Production
Compiles the app into static files for deployment.
`npm run build`

### Preview Production Build
Locally preview the build created by `npm run build`.
`npm run preview`

### Run Custom Script
Execute any script defined in the `scripts` section of `package.json`.
`npm run <script_name>`

## Maintenance & Debugging

### List Top-Level Packages
View installed packages without the nested tree.
`npm list --depth=0`

### Check Outdated
See which packages have newer versions available.
`npm outdated`

### Update Packages
Update to latest minor/patch versions allowed by `package.json`.
`npm update`

### Security Audit
Scan for vulnerabilities.
`npm audit`

### Fix Vulnerabilities
Attempt to automatically fix security issues.
`npm audit fix`

### Clear Cache
Force clear cache if installation is failing.
`npm cache clean --force`