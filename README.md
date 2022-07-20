# Svelte + Vite + Tailwindcss + DaisyUI + DateRangePicker

This is a basic svelte project with DateRangePicker 


[DEMO](https://strong-snickerdoodle-f11c54.netlify.app/)


## Steps to reproduce the project manualy

- Create svelte project with vite 
`npm create vite@latest `

- Add Tailwindcss 
`npx svelte-add@latest tailwindcss`

- Add DaisyUI plugin for tailwindcss
`npm i daisyui`

- Open `tailwind.config.cjs` file & add this line inside the plugin array `require('daisyui'),`

- Add daisyui dark theme to html 
`<html data-theme="dark"></html>`

- Install momentjs
`npm i moment`

- Install jquery
`npm i jquery`

- Install DateRangePicker
`npm i daterangepicker`

- Install node modules
`npm i`

- Start project in browser
`npm run dev` 

OR 

- To expose the ip use `npm run dev -- --host`


