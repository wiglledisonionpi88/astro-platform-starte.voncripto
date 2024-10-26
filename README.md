# Astro on Netlify Platform Starter

[Live Demo](https://astro-platform-starter.netlify.app/)

A modern starter based on Astro.js, Tailwind, daisyUI, and [Netlify Core Primitives](https://docs.netlify.com/core/overview/#develop) (Edge Functions, Image CDN, Blob Store).

## Astro Commands

All commands are run from the root of the project, from a terminal:

|# Step 1: Create the main project directory
mkdir astro-netlify-starter && cd astro-netlify-starter

# Step 2: Create package.json
cat <<EOL > package.json
{
  "name": "astro-netlify-starter",
  "version": "1.0.0",
  "description": "An Astro and Netlify starter project",
  "main": "scripts.js",
  "scripts": {
    "start": "npx netlify-cli dev"
  },
  "dependencies": {
    "netlify-cli": "^17.37.1"
  }
}
EOL

# Step 3: Create index.html
cat <<EOL > index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astro Netlify Starter</title>
    <link rel="stylesheet" href="styles/style.css"> <!-- Optional: Link to CSS file -->
</head>
<body>
    <header>
        <h1>Welcome to Astro Netlify Starter</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Features</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <h2>Main Content</h2>
        <p>This is the main content of the Astro Netlify Starter project.</p>
    </main>

    <footer>
        <p>&copy; 2024 Astro Netlify Starter</p>
    </footer>

    <script src="scripts.js"></script> <!-- Link to JavaScript file -->
</body>
</html>
EOL

# Step 4: Create .env with API keys and secrets filled in
cat <<EOL > .env
API_KEY_1='T2zcS48UbytbMqryQDZ5Ji'
API_SECRET_1='cxakp_G1EHwCmPsxYycta9KBHoJ4'
API_KEY_2='T2zcS48UbytbMqryQDZ5Ji'
API_SECRET_2='cxakp_G1EHwCmPsxYycta9KBHoJ4'
EOL

# Step 5: Create .env.example as a template
cat <<EOL > .env.example
API_KEY_1='your_api_key_1_here'
API_SECRET_1='your_api_secret_1_here'
API_KEY_2='your_api_key_2_here'
API_SECRET_2='your_api_secret_2_here'
EOL

# Step 6: Create scripts.js
cat <<EOL > scripts.js
// Basic script to demonstrate functionality
console.log("Welcome to Astro Netlify Starter!");
EOL

# Step 7: Create README.md
cat <<EOL > README.md
# Astro Netlify Starter

## Description
A starter project integrating Astro with Netlify, set up for quick deployment.

## Installation

1. Clone the repository:
   \`\`\`bash
   git clone git@github.com:yourusername/astro-netlify-starter.git
   \`\`\`

2. Navigate into the project directory:
   \`\`\`bash
   cd astro-netlify-starter
   \`\`\`

3. Install dependencies:
   \`\`\`bash
   npm install
   \`\`\`

4. Create a \`.env\` file from \`.env.example\` and add your API keys.

## Usage

To start the development server:
\`\`\`bash
npx netlify-cli dev
\`\`\`
EOL

# Step 8: Initialize Git repository and commit the setup
git init
git add .
git commit -m "Initial commit for Astro Netlify Starter project setup"

echo "Astro Netlify Starter setup complete. You can now push to GitHub." Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## Deploying to Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/astro-platform-starter)

## Developing Locally

| Prerequisites             |
| :------------------------ |
| [Node.js](https://nodejs.org/) v18.14+. |
| (optional) [nvm](https://github.com/nvm-sh/nvm) for Node version management. |

1. Clone this repository, then run `npm install` in its root directory.

2. For the starter to have full functionality locally (e.g. edge functions, blob store), please ensure you have an up-to-date version of Netlify CLI. Run:

```
npm install netlify-cli@latest -g
```

3. Link your local repository to the deployed Netlify site. This will ensure you're using the same runtime version for both local development and your deployed site.

```
netlify link
```

4. Then, run the Astro.js development server via Netlify CLI:

```
netlify dev
```

If your browser doesn't navigate to the site automatically, visit [localhost:8888](http://localhost:8888).
