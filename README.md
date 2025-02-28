# react-to-pdf-ts

This package provides a convenient and efficient way to convert React components into PDF files, leveraging the
capabilities of Puppeteer in a TypeScript environment. It is designed with a focus on ease of use, flexibility, and
robustness, making it an ideal solution for projects requiring PDF generation from React components.

## Features

- **React to PDF Conversion**: Seamlessly convert React components into high-quality PDF files.
- **Buffer Support**: No need to write to disk; you can also get the PDF as a buffer.
- **Puppeteer Integration**: Utilizes Puppeteer for reliable and accurate rendering.
- **TypeScript Support**: Full TypeScript support ensures type safety and developer-friendly usage.
- **Customizable Options**: Offers a range of customization options for Puppeteer, giving you control over the PDF
  generation process.

## Prerequisites

Before using `react-to-pdf-ts`, ensure the following is set up in your Node.js TypeScript project:

- **Node.js** and **npm** (or **yarn**) installed.
- A project set up with **TypeScript**.
- **React** and **React DOM**: Install these as they are peer dependencies of this package.

  ```bash
  npm install react react-dom

## Installation

Install the package using npm:

```bash
npm install react-to-pdf-ts
```

## Usage

Before you begin, make sure your TypeScript configuration (`tsconfig.json`) supports JSX. Set `"jsx": "react"` in your
compiler options.

Additionally, when working with JSX in TypeScript, use the `.tsx` extension for your files. TypeScript treats `.tsx`
files differently due to the JSX syntax.

Here's a quick example to get you started with `react-to-pdf-ts` in a TypeScript project:

1. **Import the package:**

```typescript
import {convertToPdf} from 'react-to-pdf-ts';
import * as React from 'react';
```

2. **Create a React Component:**

You can either define a new React component or import an existing one. Here's an example of a simple component:

```typescript
const MyComponent: React.FC = () => <div>Hello PDF World!</div>;
```

3. **Convert to PDF:**

Call `convertToPdf` with your component and specify the output path for the PDF file:

```typescript
convertToPdf(<MyComponent / >, {outputPath: './output.pdf'})
    .then((buffer: Buffer) => console.log('PDF buffer:', buffer))
    .catch(error => console.error('Error creating PDF:', error));
```

Ensure that your TypeScript project is properly set up to compile JSX.

## API

### `convertToPdf(component: React.ReactElement, options: ConvertToPdfOptions): Promise<Buffer>`

- `component`: React component you wish to convert into a PDF.
- `options`: Configuration options for PDF generation.
    - `outputPath`: (optional) File path to save the generated PDF.
    - `puppeteerOptions` (optional): Custom options for Puppeteer.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for full details.
