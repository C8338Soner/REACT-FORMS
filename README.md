# REACT-FORMS

tailwindcss
npm i -D tailwindcss
npm i -D autoprefixer
npx tailwindcss init -p
!!!WARNING DON' t FORGET ADDING THESE "
@tailwind base;
@tailwind components;
@tailwind utilities;
TO index.css top of the code.

npm i -D @tailwindcss/forms
and create a file in root (tailwind.config.js) add

<!-- /** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./src/**/*.{js,jsx,ts,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [require('@tailwindcss/forms')],
}; -->

Create a file called ContactPage.tsx in the src folder
