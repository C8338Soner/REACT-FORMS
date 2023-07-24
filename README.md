# REACT-FORMS
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
