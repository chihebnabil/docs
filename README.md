---
title: Next-Lovable v0.0.6 and Earlier
version: 0.0.6
---

An intelligent CLI tool to automatically migrate React applications to Next.js 13+ (App Router), specializing in React Router to App Router conversions.

## Key Features

- Smart React Router to Next.js App Router conversion
- Automated migration from Vite to Next.js build system
- Intelligent component transformation with `use client` directives
- Automatic handling of:
  - Route configurations
  - Layouts and page structures
  - Package dependencies
  - React Helmet to Next.js Metadata
  - Client/Server component separation

## Prerequisites

Before using the tool, make sure you have:

- Node.js 18.x or higher
- npm or yarn installed
- A [nextlovable.com](https://nextlovable.com) account
- A React project using:
  - React Router
  - Vite
  - TypeScript (optional but recommended)

## Installation

To install Next-Lovable globally:

```bash
npm install -g next-lovable
```

## Authentication

The tool requires authentication with your nextlovable.com account:
- You will be prompted to log in the first time you use it
- Sessions are stored securely for future use
- Tokens are refreshed automatically

## Usage

### Basic Command

```bash
next-lovable <source-directory> [target-directory]
```

### Dry Run Mode (Recommended First Step)

```bash
next-lovable ./my-react-app --dry-run
```

The `--dry-run` option provides:
- Complete project analysis
- Detailed migration report
- Warnings about potential issues
- List of files to be modified
- Preview of transformations
- No actual changes made

### Full Migration

```bash
next-lovable ./my-react-app ./next-app --yes --install
```

### Available Options

- `-y, --yes`: Skip confirmation prompts
- `-i, --install`: Install dependencies after migration
- `-d, --dry-run`: Run in simulation mode without making changes
- `--help`: Show help information

## Migration Process

1. **Authentication & Validation**
   - Verify your account
   - Validate the project structure
   - Check dependencies

2. **Smart Analysis**
   - Analyze route structure
   - Classify components
   - Detect context providers
   - Identify client/server boundaries

3. **Automated Transformations**
   - Convert React Router to App Router
   - Create layout structures
   - Migrate components
   - Update dependencies
   - Generate configuration files

4. **Post-Migration Setup**
   - Configure Next.js
   - Adjust TypeScript settings
   - Prepare the development environment

## Intelligent Features

- Component analysis for `use client` directives
- Automatic migration of context providers
- Preservation and enhancement of layout structures
- Dependency resolution and cleanup
- TypeScript support and type preservation

## Post-Migration Steps

1. Review the generated files in `src/app`
2. Run `npm run dev` to start the development server
3. Test your routes
4. Verify component functionality

## Limitations

- Complex custom route configurations may need manual adjustments
- Dynamic route parameters may require review
- Some third-party integrations may need updates
- Complex state management setups may need fine-tuning

## Best Practices

1. Always run `--dry-run` first
2. Keep a backup of your original project
3. Review generated files before deployment
4. Test thoroughly after migration
