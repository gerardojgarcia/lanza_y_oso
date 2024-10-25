# Lanza y Oso

Lanza y Oso is an online art studio built using Nuxt 3 and Vue 3, leveraging the latest web development practices. This project emphasizes a modern, performant, and visually appealing web experience, styled with Tailwind CSS.

## Project Setup

This project is powered by the following technologies:

- **Nuxt**: A Vue 3-based framework that enables server-rendered and static web applications.
- **Vue**: The latest version of Vue.js, utilizing the Composition API for a more structured and efficient development workflow.
- **Vue Router**: Official Vue.js router, managing client-side routing.
- **@nuxt/image**: For optimized and responsive image handling, ensuring fast load times for artwork and visuals.
- **@nuxtjs/tailwindcss**: Tailwind CSS integration for flexible and intuitive styling.

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) (version 14 or above) and npm (or yarn) installed.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd lanza-y-oso
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

## Available Commands

Here are the npm scripts available for this project:

- **Start Development Server**:
  ```bash
  npm run dev
  ```
  Starts the development server for local development at `http://localhost:3000`.

- **Build for Production**:
  ```bash
  npm run build
  ```
  Compiles the application for production deployment.

- **Generate Static Site**:
  ```bash
  npm run generate
  ```
  Creates a fully static version of the site, ready for deployment on any static hosting service.

- **Preview Production Build**:
  ```bash
  npm run preview
  ```
  Allows you to preview the production build locally.

- **Post Install**:
  ```bash
  npm run postinstall
  ```
  Prepares the application post-installation.

## Configuration

### Tailwind CSS
This project uses Tailwind CSS for styling. Check the `tailwind.config.js` file to customize or extend the default Tailwind setup.

### Nuxt Configuration
Configuration for Nuxt is located in the `nuxt.config.ts` (or `.js`) file. This file manages plugins, modules, and overall project settings.

## Usage

After running `npm run dev`, access the application at `http://localhost:3000`. The site will automatically reload as you make changes to the code, allowing for a smooth development experience.

### Deployment

To deploy the app, first build it with:
```bash
npm run build
```

Then, follow your hosting provider’s guidelines for deploying a Nuxt 3 application.

## Learn More

To deepen your understanding of the technologies used in this project, refer to the documentation:

- [Nuxt 3 Documentation](https://nuxt.com/docs/getting-started/introduction)
- [Vue 3 Documentation](https://v3.vuejs.org/guide/introduction.html)
- [Vue Router Documentation](https://router.vuejs.org/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## License

This project is private and intended for internal use by Lanza y Oso.
```

Feel free to tweak any sections to better match your project's identity and requirements!.
