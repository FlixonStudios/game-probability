# Game Probability Advisor (GPA)

## Summary

Game Probability Advisor (GPA) aims to provide calculation of probabilities wrt games.

As different games have different relevant probabilities, the idea of this app is to have different modules representing different games.

Currently, the only module available for calculation is this:
- ./Oathsworn-module.md

Please refer to the above md files for more explanation of the module.

## Installation

To run this app locally, follow these steps:

Clone the repository:

1. fork and clone the repo

2. Install relevant packages, see ./Installation.md

3. Install the dependencies:
```
cd your-repo
npm ci
```

4. Choose how you want to run the development server:
npx expo start

- If starting web
npm run web

- If starting android: 
npm run android

- If starting built locally:
npm run build:web
npm run built:web

Then open http://localhost:3000/game-probability/ (not the bare root).

The web build is exported with `experiments.baseUrl` set to `/game-probability/` (see ./app.json) so that it works on GitHub Pages, which hosts the app under that path. This means the built `index.html` requests its JS from `/game-probability/_expo/...`, so serving `dist` directly at `/` will not work. `built:web` therefore copies `dist` into `.serve/game-probability/` and serves `.serve` instead, with a copy of `index.html` at the root of `.serve` so that deep links (e.g. `/game-probability/main/oathsworn/skill-check`) fall back to the app.

If the repo is renamed, update `baseUrl` in ./app.json and the folder name in the `built:web` script to match.

Note: You should not need run other scripts if you're not planning to push to playstore

## Try it on web:

https://flixonstudios.github.io/game-probability/main/oathsworn/skill-check

## Try it on Android:

Currently app is still in internal testing and will not be available for public download.

To try the app out, drop a mail to me at flixonstudios+GPH@gmail.com

## Technologies Used

Expo: A platform for building and deploying React Native apps with ease.
React Native: A framework for building native apps using React.

Libraries:
Styled-components: For styling React Native components.

## License

This project is licensed under the MIT License.
